# MadLib Project
Task:
-Mad Libs, it takes a story of your choice, and then allows the user to replace words with (hopefully) far more hilarious words!
You, as a developer, ask the user, who hasn't seen the story, to fill in the blanks with adjectives, nouns, exclamations, colors, verbs, etc., and after these words are inserted into the blanks, the story can be read aloud to hear the hilarious results.


## Part 1: Preparation for the assignment:
Before continuing, you should attempt to do some decomposition. If you are not familiar with decomposition, it is the practice of analyzing the problem(s) in front of you. Ask yourself:

•	What needs to happen in my app, generally?
•	How might I achieve this using the tools I've learned so far?
•	Are there any situations I need to look out for - any problems this program might encounter?

## Part 2: Coding Instructions:

The Story
1.	Store the given story is story in your code file twice:

o	once in a variable (something like originalStory);
o	and once at the end of your code file in its original form, commented-out (because it's always good to have the original available for reference etc. in case you make a mistake later).

2.	Declare a variable that stores an array. You are eventually going to store the user's answers in this array, and then incorporate them into the final story. We suggest you name it something like userInputs.

3.	Identify parts of that story you would like to replace. For any noun, verb, adjective, etc. that you'd like the user to (re)define, replace that word word using template literals with a unique variable - we suggest ${userInputs[x]}. Increment 'x' by 1 for each new word/phrase you intend to replace.

4.	Check your work. Add a command to show the story in your web browser's developer console (so that we can check for errors - note that you will be looking at this for most of your project, so keep it open with F12).

5.	Once everything looks good, add, commit, and push your work to GitHub. Commit with a message like "Added mad-lib replacement variables to story".

6.	Record the number of unique replacements you're going to make, so, once you have inserted all of your tag functions, tally them up and store that number in a variable (numberOfQuestions).
User Prompts
1.	Create user-prompts for each mad-lib replacement, e.g. "Enter a verb", "Enter a noun", etc. 
2.	Store these strings in a variable (named "questionArray").
3.	Create the logic that will store the user inputs in the correct variables.
   1.	Write a 'for' loop.
   2.	Inside your loop, log 'i' to the terminal to make sure your loop is working properly.
Hints:
•	Give the following parameters: (let i = questions; i >= 0; i--)
•	Remember that in order to create a list of things for our 'for' loop to do, we need to add curly-braces after our parameters. You should have 'for (let i = questions; i >= 0; i--) { console.log(i);}'
5.	Now that we know our 'for' loop works, declare a variable *outside of the 'for' loop* that is set to 0 (named questionCounter).
6.	Next, inside of your loop, increment this variable by one, and log it (because we need a number to go up by one, and allow us to read each element of our questionArray).
7.	Again, add, commit, and push.
8.	Once you've confirmed that your loop both decreases your 'i' variable and increases your questionCounter variable, make your loop log a third thing: an element of your question array, based on your questionCounter variable (now, your loop should be able to log the first question to terminal, increase the counter by one, and then read the next question - over and over - because we are using the counter to indicate which index place in our array we'd like to read. We originally set it to '0', so our loop looks at the first position in our questionArray, and then we update the counter in order to have it look at the second position in our array; and so on.).
Note: you will want to put this line prior to increasing the counter in order to not accidentallyaccidentily miss your first question (you *don't* want to increase from 0 to 1 *before* reading from your questionArray - you want to read the zero-th index (of your array) *first*, and *then* increase the counter).
 
9.	You should now be seeing each question in the console - if you aren't, it's time to start debugging.
10.	Guess what? Add, commit, and push!
11.	For a better user experience, you can take this opportunity to tell the user how many questions / word-replacements they have left to answer immediately after being shown the current question: add a string that uses a tag function to concatenate your "questionsTotal" and helpful language (ie console.log(questionArray[questionCounter] + `(${questions} questions left)`).
12.	In order to make this go down, add a command right after to decrement the variable (questionTotal --;).
13.	Once everything works in this section, git add, commit and push.
14.	Also, you may wish to turn off all of your log to console commands *except* the "question" one ( console.log(questionArray[questionCounter] + `; (${questionTotal} questions left)`); ).
15.	Annnnnd add, commit, and push!





## Part 3: User Inputs:

1.	Inside of our loop, copy our remaining log-to-console command and replace its console.log with the prompt method (this will create a pop-up window with our questions, and a field for users to enter things).
Hint: you should now have the following line:
prompt(questionArray[questionCounter] + `... (${questionTotal} questions left)`);

2.	Store the user's input in our userInputs variable, using the .push method.
Hint: userInputs.push(prompt(questionArray[questionCounter] + `... ({questionTotal} questions left)`));
 
3.	Add a line immediately after logging-to-console the contents of your userInputs variable and check to see whether it successfully grows with each input.

4.	 If everything's working ... add, commit, and push!

5.	Using the 'alert' method, add a notice for the user that they've finished giving madlib inputs (and the story is ready) - something like alert('All done! Ready for your totally-accurate, not-at-all confusing history of tech??');

## Part 4: Final Polish:
In order to add polish and make this project a part of your online portfolio of work, you need to do a few additional things:
1.	Convert your paragraphs to HTML-ready elements (add <h2></h2> tags to the beginning and end of each paragraph).
2.	Add an instruction to print the story to the webpage with document.write(originalStory); (put it after you console.log the story).
3.	If you haven't already, now is the time to go back and do a final polish on your work - delete the original nouns, verbs etc in your story so that only the tag functions remain (you want '{userInputs[0]}' instead of 'In 1947 ${userInputs[0]}').
4.	For the last time (for now) add, commit, and push!
5.	You can come back later and add additional polish (change the CSS of your HTML file to get fancy text, colors, and even a background!).
6.	Bonus: can you add a conditional to your loop that checks whether the user's input is blank? - if it is, have it log something about "the user didn't write anything", and otherwise, have the loop store the input as normal.

