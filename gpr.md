# Claude Command: Create a Pull Request

This command is used to create a pull request on Github from the current branch to the default branch (which is usually main or master).

## What to do
1. Find the name of the default branch in the project.
2. If you are already on the default branch:
  - If there are uncommited changes, then create a new branch. 
  - If there are no uncommited changes, then exit telling the user that there are no changes to create a pull request for.
3. Commit the changes using the /gc command.
4. Push the changes to the remote repository. This step may involve creating a new branch, or pushing to an existing branch.
5. Create a pull request on Github pointing to the default branch. You can use the `gh` command line tool to do this. The pull request description and title must be well written based on the diff between the current branch and the default branch.
