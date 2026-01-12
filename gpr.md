# Claude Command: Create a Pull Request

This command is used to create a pull request on Github or Gitlab from the current branch to the branch that this branch was created from.

## What to do:
1. If there are uncommited changes, then exit the flow with an error message.
2. Determine if this is a Github or Gitlab project. If it's a github project, then use the `gh` command line tool. If it's a gitlab project, then use the `glab` command line tool.
3. Find the name of the branch that this branch was created from. Note that this is not always the default branch of the project. The branch that this was created from will be the target branch of the PR.
4. Create a pull request pointing to the branch that this branch was created from. The pull request description and title must be well written based on the diff between the current branch and the branch that this branch was created from.
5. If before this command, the PR already existed, make sure the title and descriptions are correct and updated based on the diff between the current branch and the branch that this branch was created from.
6. CRITICAL: Finally, if you think the Pull request is interesting (not just fixing typo, or adding a comment, or a small refactor), run the "/log <detailed_information_about_the_commit(s)>" command as a sub agent. Make sure that <detailed_information_about_the_commit(s)> is a proper description of the pull request in detail and contains information about the project in general. It MUST also contain the full path of the location of the project (on my local machine) so that later on another process can refer back to this project directory if needed. The purpose of this is to help maintain a log of all interesting things I did over time so that it can be converted to interesting blog posts for twitter articles and for my own website.