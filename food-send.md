# Claude Command: Send meal plan on whatsapp for tomorrow.

The purpose of this command is to send the meal plan on whatsapp for tomorrow.

## High level plan
There is a repo here on this machine: `/Users/rishabhpoddar/Desktop/trythisapp/diet`. It contains a json database, some scripts and a readme.md file. Using this, you should be able to do everything needed for the task.

## What to do
1. Find out what day of the week is today using the `date` command.
2. Read the readme here: `/Users/rishabhpoddar/Desktop/trythisapp/diet/README.md`.
3. Now, get tomorrow's meal plan by running the script `cd /Users/rishabhpoddar/Desktop/trythisapp/diet/ && node get-tomorrow-plan.js`. This should return the meals in hindi, but if there are any ingredients or meal names that are not in hindi, then convert them to hindi, and modify the `/Users/rishabhpoddar/Desktop/trythisapp/diet/ingredient-translations.json` file accordingly to include the new translations.
4. If "$ARGUMENTS" is not an empty string, then use what it says to modify the meal plan generated from the above script if needed. For example, it may say something like "dinner is out", which means you would edit the meal plan to remove the dinner meal and say something in hindi indicating that dinner is out.
5. Once the meal plan is ready, run the `cd /Users/rishabhpoddar/Desktop/trythisapp/diet/ && node send-whatsapp-message.js` such that you send up to 4 messages one after the other:
    - First message (MUST BE SENT) is a divider like ======<Day of week tomorrow in hindi>======.
    - Second message is the breakfast meal plan (this should clearly state its for breakfast, the name of the meal and the ingredients + their weights - all in hindi). If this meal is not in the output of the script, do not send this message.
    - Third message is the lunch meal plan (this should clearly state its for lunch, the name of the meal and the ingredients + their weights - all in hindi). If this meal is not in the output of the script, do not send this message.
    - Fourth message is the dinner meal plan (this should clearly state its for dinner, the name of the meal and the ingredients + their weights - all in hindi). If this meal is not in the output of the script, do not send this message.
6. Finally, if you have modified any script / json file during the workflow, then git add, commit and push the changes to the remote repository.

CRITICAL: Do NOT edit the `diet-database.json` database during the workflow under any circumstances!