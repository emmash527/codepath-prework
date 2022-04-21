# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Emma Ashton**

Time spent: **3** hours spent in total

Link to project: https://glitch.com/edit/#!/extreme-quixotic-sundial?path=index.html%3A1%3A0

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked.
* [X] Game buttons each light up and play a sound when clicked.
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [X] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
Losing with 3 strikes:
![](http://g.recordit.co/YEVElvdirE.gif)
Winning(note the pattern is randomized):
![](http://g.recordit.co/DCAxn44SKs.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.
[YOUR ANSWER HERE]

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)

  One thing that I struggled with was a logic error in my guess() code. I made a small mistake in the if statements that caused me to overflow the length of the pattern and cause the game to never end unless I clicked a random button. I fixed this by checking the console to see if I had any error messages. It did and it told me there was a bug in lightButton(). I then traced up the function calls to see where this originated, and it indicated that there was something wrong in guess(). Using this information, I slowly went through each step of the logic and noticed I was referencing outside the bounds of an array, and fixed it.

  I also had a problem with it treating the pressing of button 4 as wrong always. I opened the console and saw it though every press of button 4 was seen as a press of button 1. I then went through everywhere I wrote code for button 4 to see if I missed a 4, but there was no issue anywhere. I then decided to just refresh the page and this fixed the problem. I assume that there was some problem with the auto-refresh and it needed to be done manually.


3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)

  I have had very little experience with web development before now, but enough to be at least somewhat familiar with everything that was done in this project. I would love to know more about accessing databases. I have no experience with SQL or any other type of database programming language. I also would love to know more about the back-end side of web development like hosting a website and having a large number of users who can use the site concurrently and interact with each other. I would also like to know what the standard practices for web design in a team are. How is work divided, are there any standard practices for commenting or formatting, how do you make sure one person’s CSS or JS doesn’t affect unintended pages, etc?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)

  I think it would be really interesting to have a version of the game that can run indefinitely. Instead of generating all of the guesses at the start of the game, after each guess, it would generate a new guess to add to the end of pattern. I would also keep track of the high score and have that stored so that it is visible to all users. I would need to make sure the clues don’t get too short and update the length of the array. Another change I would make would be to have the player know how many strikes they have left. I would have it display an image of an X adjacent to the stop button for every strike so the player isn’t surprised when they lost and didn’t realize they got something incorrect.



## Interview Recording URL Link

[My 5-minute Interview Recording](https://www.loom.com/share/7b5d4a5a4831406b960ee6d758da9490)


## License

    Copyright Emma Ashton

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
