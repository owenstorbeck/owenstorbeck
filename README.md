Project Name:
Run Diary
Name:
Owen Storbeck
Description:
An app that allows a person to track the distance and the times that they log in when they go for runs as exercise.  What I want to do is allow the person to log in the times and keep them as in like a journal.  Then they can put the distance in and get a generated pace from every mile as well (so time/mile average for each run).  What they would also do is try to compare what they have either daily, weekly, or monthly.  So they track progress, but I wanted to also add in a descripton.  Like a rate of the run they go on, from a bad, okay, good, or great scale (an if statement needed). Then depending on the user-rating of the run, there is advice given from the app on what they should do, like stretch more before, rest longer, drink more water before and after, etc.
I want to build this because recently, I got into running from a friend, and I use an app that tracks my runs, but I want a more personal experience with it,  as the RunTracker app that I use does track my pace and calories, but doesn't give the questions (personal feel) that I want to bring to the table.  Calories would be hard to track, as the app is more for journaling runs, so it would be better to leave that aspect out in return for the personal run diary I want to make.
I want to make it look like a diary, but instead of using it normally, it is just for runs, with the runner's input and the progam's output sharing a page as one day's log.  So I want to have the prorgam say feedback under the runner's description of the run and their rating, like for example:

Run #: number of the run the person went for
Day: date of run
Miles Ran: miles the person ran
Minutes Went: minutes the person ran
Average Pace: pace of the runner (minutes/miles)
Improvement: Yes or No - a fun way of telling the runner if their run was better from the last one
Was the Run: Bad, Okay, Good, or Great? - scale of rating
Run Description: user's thoughts on the run that can maybe be judged by the program along with the rating
Suggestions: program's reaction based on the rating and tone of description

UML Class:
![image](https://github.com/user-attachments/assets/e89767df-d2ee-426b-a2a7-21b94683b007)
I will design everything. So the user input of the run number, date, miles ran, and minutes went all is simply scanned by the programmed and shown in the output.  The run rating is input from the user, but then correlates with the run desciption and suggestions, as whatever is put can decide what the program outputs at the suggestions, along with keywords in the description, with is also String input from the user and can be however long the user wants to make it.  The average pace is the program calculating the minutes/miles for the run.  The suggestions act as a way for the user to learn what they should keep doing for the future of their runs.  So if a rating is bad, and the description has keywords like "ache", "too long", or "uncomfortable", then suggestions might output "From what has been said, stretch, hydrate, and rest for the next run.  Don't get down, just be ready for the next one!".  I really want a therapy session almost, but it is just through the run, and from connecting the rating and description through the suggestions, then the user would get that.  You also get that from the improvement setting, as the program will tell the runner if they were better or not compared to the last run they took, with sticks with the program like a diary entry.
User --> MileAmount int, MinuteAmount int, RunRating int, RunDescription String, DateofRun String, RunNumber int
Progam --> AveragePace int, Suggestions String, NewPage String, RunUpdate String, Improvement String
Text --> RunOutput String
Plan:
The process will be hard, especially getting the suggestions to work from keywords and the rating, especially with the run entires needing to be kept for the improvement statement used as the main progress tracker.
I will be trying to implement the diary aspect last.  Then the suggestions will come after that as they will tie in two other classes.  The class of the entries has to be pulled in with the improvement class, so that comes in last no matter what, as making classes for everything else as user input would be easier than that.  Possibly best to get those out of the way due to them being simple user inputs.  The classes with the set of user inputs of miles ran and minues went tie into the average pace, and are 
