# Claude Command: Create a Pull Request

This command is used to create a pull request on Github or Gitlab from the current branch to the branch that this branch was created from.

## What to do:
1. If there are uncommited changes, then exit the flow with an error message.
2. Find the name of the branch that this branch was created from.
3. If the current branch is the default branch of the project (main or master for example), then exit the flow with an error message.
4. Otherwise, create a pull request on pointing to the branch that this branch was created from. You can use the `gh` command line tool if this is a Github project. If this is a Gitlab project, then you can use the `glab` command line tool (Make sure you run `glab mr create --help` to see how to create a MR). The pull request description and title must be well written based on the diff between the current branch and the branch that this branch was created from.
