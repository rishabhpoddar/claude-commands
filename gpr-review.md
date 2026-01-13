# Claude Command: Review a Pull Request

This command is used to review a pull request on Github or Gitlab. The pull request link is in this string: "$ARGUMENTS".

## What to do:
1. Determine if this is a Github or Gitlab project. If it's a github project, then use the `gh` command line tool. If it's a gitlab project, then use the `glab` command line tool.
2. Go through all the comments in the pull request (resolved / collapsed or not).
3. For each comment, see if it has been addressed in the code changes.
4. Report all unaddressed comments, if any. A comment is unaddressed if it's not implemented, or if it's implemented in a buggy way.

IMPORTANT:
- Make sure to use the --help flag to get the help for how to use the commands.
- Do NOT clone the repository on the local system. All information you want about the PR can be pulled in using the CLI tools.