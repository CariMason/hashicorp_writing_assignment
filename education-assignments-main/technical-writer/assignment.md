## Overview

This is a technical writing and editing project as part of your interview.

This project is designed to take between 1 - 2 hours.
Please take the time to carefully review the [writing style guide](../styling-guide-snippet.md).

## Instructions

Create a new GitHub repository with the following content (See [content](#content)) as the first commit. Make a branch and open a PR to edit the text for clarity, and include any questions about the content's meaning, as if you were editing a colleague’s work. 

 **Any changes that you think will improve the text and explain the concepts better are welcome**. If anything in the text doesn’t match your opinion on a best practice, feel free to correct the meaning of the text. The result should be a document that you, as a technical writer, would be comfortable sharing with end-users.


Construct your PR to teach the author:
- Make atomic commits.
- Write your commit messages to show your rationale for edits.
- Please construct your commits, commit messages, and PR description as you would for an actual PR as if you were collaborating with a team.
- It is best to edit the files on your local machine and push with the `git` command or a desktop Git application rather than editing directly on the GitHub.com website.

Edit the text so that it is easy to read:
- Correct errors.
- Put the text in active voice and present tense.
- Address the reader as you, not we.
- Phrase statements as positive rather than negative.
- Make the language simple and plain. 
- Avoid euphemisms.
- Structure the text so it has a logical flow. 

Once you're finished with your edits, send the PR link to the HashiCorp recruiter.

**NOTE**: DO NOT FORK THE PROJECT. MAKE A COPY OF ALL FILES, CREATE YOUR OWN FRESH REPOSITORY AND SUBMIT A PULL REQUEST TOWARDS YOUR OWN PROJECT. DO NOT MERGE THE PULL REQUEST.

---

## Content

### What is the difference between push, pull, and fetch?

Push, pull, and fetch are commonly used Git commands that allow you to to make changes to a shared repository. 

- `git push` - Publishes changes from a local repository to a remote repository. The changes update the remote repository to resemble your local branch. 
- `git fetch` - Safely downloads commits, files, and references from a remote repository into your local repository. It does not automatically merge them.
- `git pull` - Fetches and merges the remote repository to your local file. This action can overwrite local changes that have not yet been committed.


If the remote branch has diverged from your local branch, the `git push` command will fail with the following message: error: Your local changes to the following files would be overwritten by merge.

**NOTE**: The `git status` command safely displays any differences between the local and remote branches. 


If `git push` fails, you can overwrite your local changes using `git pull` or you can preserve your local changes using the following commands:

`git fetch` - Brings the diverged changes to your local branch without merging them.
`git stash` - Saves your local changes.
`git merge origin/master` - Integrates the changes from the remote and local branches. 
`git stash pop` - Brings your local changes back and removes the stash commit.
