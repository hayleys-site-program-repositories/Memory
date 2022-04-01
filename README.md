# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Hayley Simmons**

Time spent: **24** hours spent in total

Links to project: (https://glitch.com/edit/#!/a-memory-game [code], https://a-memory-game.glitch.me [live site])


## Required Functionality

The following **required** functionality is complete:

* [Y] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [Y] "Start" button toggles between "Start" and "Stop" when clicked. 
* [Y] Game buttons each light up and play a sound when clicked. 
* [Y] Computer plays back sequence of clues including sound and visual cue for each button
* [Y] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [Y] User wins the game after guessing a complete pattern
* [Y] User loses the game after an incorrect guess

The following **optional** features are implemented:
`
* [Y] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [Y] Buttons use a pitch (frequency) other than the ones in the tutorial
* [Y] More than 4 functional game buttons
* [Y] Playback speeds up on each turn
* [Y] Computer picks a different pattern each time the game is played
* [Y] Player only loses after 3 mistakes (instead of on the first mistake)
* [Y] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [Y] List anything else that you can get done to improve the app!

	~ While the clue sequence is actively playing, the buttons are disabled from user clicks. When the sequence is finished, buttons are enabled for guessing again.


## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:

~ [winning gif](https://media.giphy.com/media/bcbwLQxFSdW1OGwZoV/giphy.gif)

~ [losing gif](https://media.giphy.com/media/EaSAsnhHA1ywP0zfCx/giphy.gif)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

	~ A professor of mine (thank you Dr. Edwards!)
	~ CodePath TA, Anitya Gupta

	~ [How to center a button in CSS](https://www.javatpoint.com/how-to-center-a-button-in-css)
	~ [CSS references](https://www.w3schools.com/cssref/)
	~ [Random in Javascript](https://www.w3schools.com/jsref/jsref_random.asp)
	~ [Settimeout in Javascript](https://www.w3schools.com/jsref/met_win_settimeout.asp)



2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

	~ My first challenge was recreating the guess function to include user mistakes. I wanted the function to replay the sequence after the user makes a mistake, add to/subtract from the mistake counters, & when the user made their 3rd mistake it was immediate game over.  What ended up happening, however, was that once the user reached 3 mistakes the clue sequence still replayed. It was only after the user clicked a button, right or wrong, that the game ended. The problem was the order of my if-statements. My professor helped me in realizing this mistake. I solved this problem by first turning the if-statement for checking incorrect buttons into a nested if-statement. The nested if-statement then checked if the user had 3 mistakes, only playing the sequence if it was false. The rest of the code for checking correct buttons was made into an if-else statement.
	
	~ My second challenge was disabling the buttons during the clue sequence to prevent users clicking them. I had trouble figuring out where to specifically put the code; I thought simply saying in the guess function that if the clue sequence was playing, set “button.disabled” to true, & if it was not playing then set “button.disabled” to false. But it was a little more complicated than that. I had help from a CodePath TA & a fellow SITE applicant who also tackled this problem. I solved this problem by approaching it similarly to adding the “lit” class: creating two functions, one for enabling (enableButtons) & one for disabling (disableButtons). I then had to place them in the playClueSequence function. My next minor issue from here was that I was supposed to setTimeout the enableButtons function, rather than the disableButtons function. When I tried to setTimeout the disableButtons function, it only disabled the one button & the buttons didn’t re-enable again despite putting it into the end of the function.
	
	~ My third challenge was that I had an unexpected, but minor, bug come up. The button tone would keep playing if the button was accidentally dragged. It didn’t stop unless I refreshed the page or clicked the button once more. For the sake of time, I unfortunately did not fix this problem. I pray no one accidentally drags it.  



3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)

	~ My first question about web development would be on how to start a portfolio. I would like to know how one goes about starting new projects, the types of projects, etc. And what are good, preferably free, websites to host said portfolios. 

	~ My second question is what careers in web development would look like when “create-it-yourself” websites are becoming more readily available. If someone would like to be a freelance web developer, then I would like to know how to make yourself more competitive against said websites.

	~ My third question is on how to write better code. Specifically, I would like to know ways to avoid hard-coding solutions. I know that brittle code is not necessarily bad, however it is a struggle to deal with when trying not to break something dealing with something else.

	~ And my fourth question is about why I had to setTimeout the "enableButtons" function instead of the "disableButtons." It only halfway makes sense: disabling, then enabling them after a certain amount of time. But I don't fully understand why you couldn't do the opposite: having them enabled, then disabling them for a set amount of time. 



4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

	~ If I had a few more hours to work on the project, I would start by changing the button tones to piano chords simply because it would sound much prettier. Adding a seperate sound and/or visual indicator to indicate a wrong answer would also be ideal. Since my game is space-themed, I would prefer to have 3 aliens (instead of Xs) indicate wrong answers. Each wrong answer would turn each alien white; it would be a blank outline otherwise.
	
	~ Next, I would tackle the slight problems of the pattern speeding up despite the user having made a wrong guess and it is merely repeating, and the button tones starting and not stopping when accidentally dragged.
	
	~ I would then implementing a timer feature to limit the amount of time a user has on guessing patterns. This would most definitely increase the difficulty of the game. It would then tie into creating different difficulty levels that the user can choose from. My ideal “Easy” mode would be to have 4 buttons, 3 chances, sequence length of 8 numbers, & 30 seconds per round. “Intermediate” mode would have 6 buttons, 2 chances, sequence length of 12 numbers, & 20 seconds per round. “Advanced” mode would have 8 buttons, 1 chance, sequence length of 16 numbers, & 10 seconds per round. 
	
	~ If I had more than a few hours, I would then like to implement a “high score” system in the game. There would be a database of high scores separated by difficulty level. When the user beats their high score in a game, it would congratulate them on the new high score & update the database. This could also tie into creating an “Endless” mode, where the pattern could continuously keep going (making the pattern length an absurd number like 1000). This mode would only time the rounds, maybe for 1 minute each, instead of going by mistakes. The user would just focus on beating their high score.


## Interview Recording URL Link

~ [My 5-minute Interview Recording](https://drive.google.com/file/d/1YBzEBfM_VDKbbg0H2JZC5riOZbsT-8Dm/view?usp=sharing)


## License

    Copyright [Hayley Simmons]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
