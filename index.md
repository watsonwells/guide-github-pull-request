# Making an Epic Pull Request

Having a your first pull request (PR) accepted to an open source project is one of the best feelings there is when it comes to working with open source code. There's nothing like working with other people, contributing to a project you care about, and showing off your crazy coding skills through a great PR. This guide will establish some guidelines on how to make your PRs amazing, so read on if that seems up your alley!

### Finding A Project to Contribute To

A lot of people ask me how to find a project to contribute and/or make a pull request to. Luckily, this question has an easy answer: contribute to projects you use. You should not be browsing github for random projects and trying to contribute to one of them. You should write code as you normally do, use other peoples' libraries, and when you find a bug or something you'd like to add, then think about contributing.

Contributing to open source projects should be an entirely natural and logical process. Here's some code you use, here's a specific thing you see that would make it better, let's go and contribute. If you haven't found any issues with any of the libraries you use, that's awesome, they must be super solid. If you don't use a lot of other peoples' projects, you probably are just starting out with coding. Keep practicing and getting better, and as you do so you will gradually try out and use more third-party projects.

### If in Doubt, Ask

So let's say that you have an idea for a great feature for a project that you use, that would make you life (and presumably others' as well) much easier. Seems like a good time to clone that code down and see if you can make a pull request, right?

Well, not quite. Before you do this, it's a good idea to **ask**. What if the author of the code has a good reason they don't want to add that feature, it's already in progress, etc? Generally if you want to be safe, before opening a pull request or starting to work on code in someone else's project, its a good idea to first open an issue and ask about it. For example, if you are thinking about a new feature, you could describe the feature, say you are happy to open up a PR for it, and ask the code author's opinion. If they agree, go for it! They might even have some good suggestions for changes or additions to the feature as well.

If it's a bug you found, occasionally it can be ok to just open a PR, as long as it's clearly a bug with a straightforward fix, but it's also not a bad idea to file the bug as an issue first.

Finally, if you are using a project you just love and want to contribute back to, you can ask the author if they need help with anything, or see if it's ok if you try to tackle an already existing issue. This is a great way to get involved and give back to a project you really appreciate!

### Using Branches

Ok, so we have a great feature idea, we opened an issue to check with the author, and they signed off on it. Whoo! Time to get to coding. First thing you should do is **create a branch** for your new code. This is always a good idea when working on a specific feature of fix for any project, and PRs are no exception. Make sure to name your branch with something understandable, related to the change you are making, and not too long.

### Writing a Good Commit Message

Now you have written some code in your branch, and are ready to commit. Especially when you are contribuing to someone else's project, you want to make sure to write good, clean commit messages. Let's review the anatomy of a commit message.

```
First line, no more than 50 characters

Details section, as long as you want. Not always necessary, but
available if you need it. Wrapped at 72 characters. Present imperative
tense is preferred for commits. That means "fix bug", not "fixes bug" or
"fixed bug".

- Use bullets if you need
- Bullets are a good way to summarize a few things

If you have too much info here, it might be a good candidate to break
down into multiple commits. You can use emoji here too :sparkles:
```

In order to write commits cleanly like this, it's easiest to use vim with syntax highlighting on. Vim will give you enough space to write the full message, notify you when you have hit the 50 char limit on the summary etc. You don't need to be a vim wizard to write a commit, you just need the basics.

If you are closing an issue with the commit, you might be used to using `closes #xx` or `fixes #xx` at the end of a commit. This is a great trick, but for pull requests, its better to put this at the end of your PR description field. This will accomplish the same thing, but won't notify the issue multiple times if there's a rebase.

For more detail on writing good commit messages, check out [this classic article](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).

### Code Standards

When writing both commits and code, it's important to do so in harmony with a project's existing style. So if the author has all past tense commits, your commits to the project should be written in past tense as well. If the project uses camelCase variable naming, this is how you should name your variables as well. If the project has a test suite, you should be writing tests for any changes you make.

Even if you don't agree with some of the author's stylistic decisions, you should adhere to them in your PR. If you have a solid reason why they should be changed, open up an issue and discuss it there. Never ever change an author's existing code style to something you prefer, this is in extremely poor taste.

### Rebasing

We would certainly need another article to fully cover git rebase, but when making pull requests, understanding rebase is very important. It's likely that in the course of discussing the pull request with the author and/or core team, some mistakes will be caught or changes will need to be made. In fact, this is likely even before you submit the pull request. But it's important to clean these mistakes up and represent your changes with clean atomic commits so that it's easy to review.

For example, if you made a mistake in your first commit, but fix it in a later commit, this makes it much harder for reviewers, since they will read the commits chronologically, and potentially see and point out the mistake, only to be reminded later that it was fixed. Much easier if the PR is presented without mistakes in the first place.

In addition, many authors prefer clean and organized commits to be merged into their projects, not 5 commits of fixes and corrections and one commit with the actual code making the change. Rebase allows you to clean up and compress your commits so you can make this happen.

Finally, it's best to merge branches that are based on the latest commit of the branch they are being merged into, to ensure a clean history and no conflicts. Keeping your branch up to date with the master branch also requires some work with rebase, and if not more often should at least be done before a PR is merged.

### Opening it Up

Phew, that's a lot to remember already! But let's say you have finished your PR and feel like it's ready to submit. A couple last pieces:

- Make sure the title and description are clear and concise
- If the change is visual, make sure to include a screenshot or gif
- If the PR closes and issue, make sure to put `Closes #X` at the end of the description on a newline
- Make sure it is being opened into the right branch
- Make sure it has been rebased on top of that branch

Then let's go for it and open it up!

### Work In Progress

If you aren’t totally done with the PR, make sure to add `[WIP]` to the title at the beginning to indicate that its a work in progress. In addition, make sure to note in the description what is still being worked on — you can edit this later and remove it once its done.

Try not to put up work in progress PRs for other people’s repos unless you are trying to solicit feedback or help from the maintainer getting the part done that isn’t finished yet. Usually WIP pull requests will be for your own repos though.

### Expect Review

So the pull request has been submitted, and now it's time for review. As you would if someone sends you a PR, you should expect the maintainer to be reviewing every line of code. Do not be offended by this, if they catch a mistake or suggest doing something in a different way that’s awesome, maybe you can learn something. Most people are pretty reasonable about this stuff. You guys are working together, keep it calm and casual. If you are not used to code review, it can be easy to feel offended by this process, so keep in mind that any feedback is in good sprit, and just meant to make the project better. And remember that open source is all about learning -- you can often pick up some great practices working with others.

Once all has been approved, any changes have been made, and the commits and code are clean, your PR should be ready for merge!

### Keep Tabs On The Project

Hey congrats on getting your pull request merged! If you are invested in this project, you might want to keep an eye on it in case you can help out in the future. Use the watch button on the repo and the subscribe and unsubscribe buttons on individual issues to keep up with things. Who knows, some day you might be added to core!

Congrats again on the successful pull request, and here's to many more.

