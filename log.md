# Claude Command: Help log content

The purpose of this command is to help maintain a log of all interesting things I did over time. Those logs will then be converted to interesting blog posts for twitter articles and for my own website.

## What to do
1. Ask me what I did recently.
2. If I didn't say anything, then exit.
3. Otherwise try and have a conversation with me about what I did and extract the interesting learnings and insights from it.
4. Once you have something interesting, create a new log file in `/Users/rishabhpoddar/Desktop/trythisapp/work_log/logs`. The file name should contain the current date and time in this format: `YYYY-MM-DD_HH-MM-SS.md`. You should get the date and time from the system using the `date` command.
    - The contents of the file should be a free form text of the interesting learnings and insights.
5. Once the log file is created, git add, commit and push the changes to the remote repository.

IMPORTANT: 
- Ask a maximum of 5 questions throughout the conversation.
- If "$ARGUMENTS" is not an empty string, then do not ask anything. Just use "$ARGUMENTS" as all the information you need to create the final log file.