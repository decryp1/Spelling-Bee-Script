## HISTORY OF HERKLE HUB FOR SPELLING BEE
Herkle Hub was the very first Spelling Bee script. It started out rough, with only a label that showed you the current word, a copy word button and an auto type. Upon the realization that other scripts were in development, I decided to rewrite it. The first rewrite ended with Herkle Hub being barely the best Spelling Bee script, with a few holes here and there. Only one other script had ever topped Herkle Hub, and that was when I stopped updating the script. After a few months of not updating Herkle Hub and scripts like Preppy Hub maintaining updates, I decided to do a full rewrite of Herkle Hub for Spelling Bee, which is the current version below. At the time of writing this, Herkle Hub has ZERO competition and is undeniably the BEST Spelling Bee script.

## CURRENT STATE OF HERKLE HUB FOR SPELLING BEE + SHOWCASE
Herkle Hub is the BEST script for Spelling Bee by Bean's Can. This script has over 50 features, all which work in unison with eachother to increase stability. Herkle Hub is the most precise, clean, and performant Spelling Bee script. Herkle Hub stands out with features like Auto Typo, Always Correct Letter, a built in word-logger that auto fills the word in the ui to make adding words even easier, and an Emote Player that includes all paid emotes and even the unreleased ones, ALL FOR FREE! Everything found in Herkle Hub for Spelling Bee is not only the first of its kind, but it also the BEST version of said feature! Herkle Hub does it best, and that's guaranteed. 
<img width="728" height="608" alt="image" src="https://github.com/user-attachments/assets/123d8ae1-2e52-478a-b211-062a77d290f4" />
<img width="725" height="999" alt="image" src="https://github.com/user-attachments/assets/923de645-0c2b-40f9-b31b-5a9278db4613" />
<img width="761" height="660" alt="image" src="https://github.com/user-attachments/assets/26d85b36-fe84-423f-815d-1c48cc24d9ab" />
<img width="716" height="687" alt="image" src="https://github.com/user-attachments/assets/c96b6621-151b-45a7-a38e-05ea00707c96" />
<img width="488" height="504" alt="image" src="https://github.com/user-attachments/assets/8fe35305-6994-49dc-96c2-27352b3d719a" />

# Feature Explanation
#1 "Copy Current Word"

  > sets the current word to your clipboard

#2 "Say Current Word"

  > says the current word in the chat

  > "Auto Say Word" automates this feature!

  > "Say Word Delay" changes how long the script waits before saying the current word

#3 "Auto Type" (i wont add sliders since some are already covered here, and most are just a given (also features will be "counted" based on whether or not it's a SOLE feature))
  > automatically types the current word for you
  
  > "Typing Method" changes the method the script will use to enter a key
    > "Keypress" tells the script to use the "keypress(<keycode>)" function in your executors environment
    > "Remote" tells the script to fire the games remotes to register a keypress, rather than pressing keys. this reduces interference with chats and such.
    > "VIM" does NOT use VirtualInputManager, the name is misleading. this method tells the script to, instead, edit the box where the word is entered to trick the game
    
  > "Typing Mode" changes the waiting method the script will use between keypresses
    > "Static" tells the script to wait for as long as the user tells it to, no later, no less, before and betwixt each keypress
    > "Random" tells the script to choose between a min and max value, and wait for that duration
    
  > "Typing Speed Range"
    > only visible when the "Random" typing mode is chosen
    > turns two sliders on: "Custom Min Speed" and "Custom Max Speed". these sliders let the script use the "math.random(<1>, <2>)" function to choose a random integer between the two values, and wait for that duration before each keypress

  > "Random Pretype Delay"
    > instead of waiting for a constant value every time, it chooses a value from the two sliders that show upon the state changing, and waits for that duration before typing a word

  > "Random Submit Delay"
    > tells the script to, once again, wait for a random amount of time before entering the word. randomness depends on the min and max slider values

  > "Dont Enter Word"
    > tells the script to not enter the word so you can enter it manually

#4 "Auto Typo" (sliders will be added here since it just seems right)
  > tells the auto type to incorporate minor spelling errors (typos) into the spelling of a given word, based on the chosen settings

  > "No Early Typos"
    > tells the script to wait until a certain amount of letters have been typed before typo-ing

  > "Typo Method"
    > "Correct Letter + Typo"
      > tells the script to press the correct letter in a word, but also an incorrect one to seem more human
    > "Incorrect Letter"
      > upon reading this over, i realize that this one should just be named "Typo", since thats what it is
      > tells the auto type to just press an incorrect letter for a typo

  > "Max Typos Per Word"
    > tells the auto type + typo to not add a certain amount of typos in each word

  > "Typo Chance"
    > the chance that is weighed before each keypress to determine if it should be a typo or not

  > "Typo Backspace Delay"
    > the delay after adding a typo that the script will wait before reversing the typo

  > "Typo Resume Delay"
    > 67
    > the time the script waits before pressing the next key after a typo

  > "Continue After Typo"
    > instead of instantly reversing the typo, if this toggle is on, the script will press a few more keys before reversing the typo. keys pressed during this fugue state will never be typos, only correct ones

  > "Max Letters After Typo"
    > the max letters that will be pressed for a word after a typo
    > only works if the toggle above is turned on

  > "Delete Full Word"
    > instead of backspacing over a set amount of keys, if this toggle is on, the entire word will be deleted and restarted, to make u seem like a pro

  > "Delete Full Word Chance"
    > chance that gets weighed upon the backspacing of a typo to determine whether or not it will be fully deleted

  > "Lose After X Words"
    > tells the script to PURPOSEFULLY lose after a certain amount of words have been typed

  > "Max Words Before Lose"
    > max words that must be typed before the script loses for you

  > "Lose Method"
    > the method the script will use to lose for you
    > "Enter Early"
      > enters the word early if the script is trying to lose
    > "Typo"
      > script will use a typo to lose

#5 "Always Correct Letter" (MY FAVORITE FEATURE)
  > this feature lets you press ANY KEY YOU WANT, and will turn it into the correct key for you. 
  > this feature AUTOMATICALLY enters for you if you press a key after the word has been fully typed
    > this is because the next "correct letter" after you fully type a word and dont enter, is literally to enter the word. this is also for ease of access so you can see before you enter
  > this feature is 100% undetected and can never be detected. Spelling Bee devs would have to fully rewrite their internal infrastructure to break this feature
  > this feature works on EVERY device, but not every executor. this feature is very advanced, most executors for pc that arent paid cant handle it (as of 12/4/25, 8:51 PM)
  > i cant stress how amazing this feature really is, it's truly amazing

#6 "Free Emotes"
  > lets you play any emote, even unreleased ones, for free. you can also change the speed of the emotes with HHUB

#7 "Auto Click Ducks"
  > automatically clicks ducks for you when a duck is detected

#8 "Show Admin Panel"
  > shows the admin panel on the bottom left hand corner of your screen
  > obviously this wont give u admin, its just for fun

#9 "Mod Detector" (this features needs some reworking"
  > detects when a moderator enters your game
  > "Serverhop if Mod Detected"
    > hops servers if a moderator is detected. this feature automatically executors HHUB for you in the new server.

#10 "Chat Detector"
  > detects if someone types a trigger word in the chat (e.g., hub, cheater, cheats, hacks, hacker, exploiter, etc..)
  > "Serverhop if Chat Detected"
    > hops servers if someone says a trigger word. HHUB automatically executes again in the new server
  > "Panic Mode"
    > instead of serverhopping, HHUB will turn off every toggle to not get caught

#11 "Word Logger"
  > logs every word for you, even words that are not present in the word list
  > "Clear History"
    > clears the word history
  > "Copy History"
    > copies every soundid and word in the dropdown to your clipboard
  > "Export History"
    > exports the word history to a txt file in your executors workspace folder for you to read
  > "Copy Word"
    > copies the selected word in the dropdown
  > "Copy SoundId"
    > copies the selected words' soundid if found
  > "Play Sound"
    > plays the currently selected words' soundid

#12 "Mini Mode:
  > creates a watermark near the top left corner of your screen, which shows the current word. this watermark is draggable, and made to use with the ui minimized so you can see the word in a smaller menu. mainly created for mobile users, but works on every device. highly recommended to use this
      
  
    
