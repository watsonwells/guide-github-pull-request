# Making an Epic Pull Request

A generic intro paragraph that talks about how cool open source and pull requests are. Oh yeah.

### Finding A Project to Contribute To

- Contribute to projects you actually use
- For example, when you have found a bug or a feature you want to add
- You don’t just go around trying to contribute for the sake of doing so, this doesn’t make any sense

### If in Doubt, Ask

- If you are thinking about adding a feature make sure to ask first in case there’s some reason the maintainer doesn’t want it or has already considered it etc. Don’t want to waste your time.
- If you found a bug but are not sure how to fix it, open an issue to report the bug, say you are willing to fix it but would love to get some help or a push in the right direction as you don’t entirely understand the codebase.
- Otherwise if it’s a clear bug and you’re submitting a fix, you can probably just go for the PR. Although it’s not bad to open an issue either and just say you’re working on a PR as well.

### Using Branches

- Use a branch to make your change. Submit a pull request from the branch. If something goes wrong it’s easier to revert that way.
- You should always be using branches for pull requests no matter what. If you are core on the repo, you can PR from a branch. If you are not core, fork, branch, then PR.

### Writing a Good Commit Message

- Summary, 50 chars
- Extra info section, as long as you want
- Present imperative tense
- Feel free to use bullets in your additional info section
- Feel free to reference users and/or issues as well
- "closes #x" AT THE END will close an issue when merged to master. For a PR, better to put this in the PR description than the commit message though.
- Wrap at 72 columns
- Use vim to commit for highlighting on these limits
- If you have too much in the extra info section, it may be too large of a commit
- But don't be afraid to be very clear, if it's just clarity and background you are expanding on it's fine. I've seen commits with 3 paragraphs of supplemental info.
- Emoji work in commit messages as well
- http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html

### Code Standards

- Make sure to pay attention to the coding standards that the project uses. For example, tabs vs spaces, underscore vs camel case, commit message tense, etc. Adhere to these, even if they are not naturally your style.
- Do not ever change another repo’s code style, this is in extremely poor taste.
- Don’t mix up a few different changes into one PR. If you found 2 issues, submit 2 PRs

### Rebasing

- We don’t have time here to cover rebase fully but link to some resources and look forward to potentially a git guide in the future. But make sure your commits are buttoned up before you submit.
- Including mistakes makes things much harder to review for maintainers so this is super important.

### Opening it Up

- When you feel like everything is finished (including tests, if the repo has them! this is important!), open up the PR. Make sure the title and description are clear and concise. If it closes out an open issue, make sure to put “Closes #x” with the issue number at the bottom of the PR’s description — this way it will close out the issue automatically when merged.

### Work In Progress

- If you aren’t totally done with the PR, make sure to add `[WIP]` to the title at the beginning to indicate that its a work in progress. In addition, make sure to note in the description what is still being worked on — you can edit this later and remove it once its done. Try not to put up wip PRs for other people’s repos unless you are trying to solicit feedback or help from the maintainer getting the part done that isn’t finished yet.

### Expect Review

- As you would if someone sends you a PR, you should expect the maintainer to be reviewing every line of code. Do not be offended by this, if they catch a mistake or suggest doing something in a different way that’s awesome, maybe you can learn something. Most people are pretty reasonable about this stuff. You guys are working together, keep it calm and casual.
- Once everything is approved, you should be merged in. Yay!

### Keep Tabs On The Project

- Hey so congrats on getting it merged! If you are invested in this project, you might want to keep an eye on it in case you can help out in the future. Use the watch button on the repo and the subscribe and unsubscribe buttons on individual issues to keep up with things. Who knows, some day you might be added to core!

