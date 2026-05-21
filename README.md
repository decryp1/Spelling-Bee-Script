## CURRENT STATE OF HERKLE HUB FOR SPELLING BEE + SHOWCASE
Herkle Hub is the BEST script for Spelling Bee by Bean's Can. This script has over 50 features, all which work in unison with each other to increase stability. Herkle Hub is the most precise, clean, and performant Spelling Bee script. Herkle Hub stands out with features like Auto Typo, Always Correct Letter, a built-in word-logger that auto fills the word in the ui to make adding words even easier, and an Emote Player that includes all paid emotes and even the unreleased ones, ALL FOR FREE! Everything found in Herkle Hub for Spelling Bee is not only the first of its kind, but it also the BEST version of said feature! Herkle Hub does it best, and that's guaranteed.
Home tab (greeting, stats, utility)
<img width="728" height="608" alt="image" src="https://github.com/user-attachments/assets/123d8ae1-2e52-478a-b211-062a77d290f4" />

Game tab (auto type/typo, always correct letter, pretty much every feature resides here)
<img width="725" height="999" alt="image" src="https://github.com/user-attachments/assets/923de645-0c2b-40f9-b31b-5a9278db4613" />

Extra tab (free emotes, visual mod panel, word-logging, auto ducks, and safety features. not everyones favorite, but it does what others don't)
<img width="761" height="660" alt="image" src="https://github.com/user-attachments/assets/26d85b36-fe84-423f-815d-1c48cc24d9ab" />

UI Settings tab (general visual customization, saves/configs, and Mini Mode for a less crowded screen)
<img width="716" height="687" alt="image" src="https://github.com/user-attachments/assets/c96b6621-151b-45a7-a38e-05ea00707c96" />
<img width="488" height="504" alt="image" src="https://github.com/user-attachments/assets/8fe35305-6994-49dc-96c2-27352b3d719a" />

# Feature Explanation

<details>
<summary><b>#1 — Copy Current Word</b></summary>

- sets the current word to your clipboard

</details>

<details>
<summary><b>#2 — Say Current Word</b></summary>

- says the current word in the chat
- `Auto Say Word` (found near `Say Current Word`) automates this feature!
- `Say Word Delay` changes how long the script waits before saying the current word

</details>

<details>
<summary><b>#3 — Auto Type</b></summary>

- automatically types the current word for you
- `Typing Method` changes the method the script will use to enter a key
  - `Keypress` tells the script to use the `keypress(<keycode>)` function in your executors environment
  - `Remote` tells the script to fire the game's remotes to register a keypress, rather than pressing keys. this reduces interference with chats et al.
  - `VIM` does NOT use VirtualInputManager, the name is misleading. this method tells the script to, instead, edit the box where the word is entered to trick the game
- `Typing Mode` changes the waiting method the script will use between keypresses
  - `Static` tells the script to wait for as long as the user tells it to, no later, no less, before and betwixt each keypress
  - `Random` tells the script to choose between a min and max value, and wait for a random time within that duration
    - e.g., min wait time is 0.06, max is 0.2. the script runs math.random(0.06, 0.2), and chooses a value like 0.12
- `Typing Speed Range` only visible when the "Random" typing mode is chosen. turns two sliders on: `Custom Min Speed` and `Custom Max Speed`. these sliders let the script use the `math.random(<min>, <max>)` function to choose a random integer between the two values, and wait for that duration before each keypress
- `Random Pretype Delay` instead of waiting for a constant value every time, it chooses a value from the two sliders that show upon the state changing, and waits for that duration before typing a word
- `Random Submit Delay` tells the script to, once again, wait for a random amount of time before entering the word. randomness depends on the min and max slider values
- `Dont Enter Word` tells the script to not enter the word so you can enter it manually

</details>

<details>
<summary><b>#4 — Auto Typo</b></summary>

- tells the auto type to incorporate minor spelling errors (typos) into the spelling of a given word, based on the chosen settings
- this increases the human aspect of the auto type, but is not guarenteed to nullify bans. it's not a human.
- `No Early Typos` tells the script to wait until a certain amount of letters have been typed before typo-ing
  - if the word is "definitely", the script will only allow typos after the letter "n", and no earlier.
- `Typo Method`
  - `Correct Letter + Typo` tells the script to press the correct letter in a word, but also an incorrect one to seem more human
  - `Incorrect Letter` tells the auto type to just press an incorrect letter for a typo
- `Max Typos Per Word` tells the auto type + typo to not add more than a certain amount of typos in each word
- `Typo Chance` the chance that is weighed before each keypress to determine if it should be a typo or not (like flipping a coin with odds that YOU choose with sliders, rather than 50/50)
- `Typo Backspace Delay` the delay after adding a typo that the script will wait before omitting the typo
- `Typo Resume Delay` after inserting and omitting a typo, this slider determines how long to wait before typing the next letter
- `Continue After Typo` instead of instantly reversing the typo, if this toggle is on, the script will press a few more keys before reversing the typo. keys pressed during this state will never be typos, only correct ones
  - `Max Letters After Typo` the max letters that will be pressed for a word after a typo. only works if the toggle above is turned on
- `Delete Full Word` instead of backspacing over a set amount of characters, if this toggle is on, the entire word will be deleted and restarted to make u seem like a pro
  - `Delete Full Word Chance` chance that gets weighed upon the backspacing of a typo to determine whether or not it will be fully deleted
- `Lose After X Words` tells the script to PURPOSEFULLY lose after a certain amount of words have been typed
  - `Max Words Before Lose` max words that must be typed before the script loses for you
  - `Lose Method`
    - `Enter Early` enters the word early if the script is trying to lose
    - `Typo` script will use a typo to lose

</details>

<details>
<summary><b>#5 — Always Correct Letter</b></summary>
  
- this feature lets you press ANY KEY YOU WANT, and will turn it into the correct key for you.
- this feature AUTOMATICALLY enters for you if you press a key after the word has been fully typed
  - this is because the next "correct letter" after you fully type a word and dont enter, is literally to enter the word. this is also for ease of access so you can see before you enter
- this feature is 100% undetected and can never be detected. Spelling Bee devs would have to fully rewrite their internal infrastructure to break this feature
- this feature works on EVERY device, but not every executor. this feature is very advanced, most executors for pc that arent paid cant handle it (as of 12/4/25, 8:51 PM)
- i cant stress how amazing this feature really is, it's truly amazing
- `Auto Enter if Extra Key` tells this feature whether or not to automatically enter after the word gets spelled correctly, and an extra key is pressed (useful for spamming your keyboard)

</details>

<details>
<summary><b>#6 — No Textbox Restrictions</b></summary>

- this feature removes nearly every restriction placed on the typing textbox
- this feature allows you to type any character you want (numbers, spacebar, symbols, etc)
- removes case restrictions (you can type in all uppercase or all lowercase, or a mix of the two)
- removes others' abilities to see what you type. this makes it nearly all visual for you, but others cannot see what you type, or how fast.
- removes the server-sync, so the server cant efficiently calculate your WPM or replicate your text to others
- removes typing sounds from replicating to you or anyone else, since the server-sync is gone
- removed pasting (Ctrl + V) checks, so you can paste words freely into the box
</details>

<details>
<summary><b>#7 — Free Emotes</b></summary>

- lets you play any emote, even unreleased ones, for free. you can also change the speed of the emotes with HHUB
- pssttt, unreleased emotes are js emotes i got from infinite yield

</details>

<details>
<summary><b>#8 — Auto Click Ducks</b></summary>

- automatically clicks ducks for you when a duck is detected

</details>

<details>
<summary><b>#9 — Show Admin Panel</b></summary>

- shows the admin panel on the bottom left hand corner of your screen
- obviously this wont give u admin, its just for fun

</details>

<details>
<summary><b>#10 — Mod Detector</b></summary>

- detects when a moderator enters your game
- `Serverhop if Mod Detected` hops servers if a moderator is detected. this feature automatically executes HHUB for you in the new server

</details>

<details>
<summary><b>#11 — Chat Detector</b></summary>

- detects if someone types a trigger word in the chat (e.g., hub, cheater, cheats, hacks, hacker, exploiter, etc..)
- `Serverhop if Chat Detected` hops servers if someone says a trigger word. HHUB automatically executes again in the new server
- `Panic Mode` instead of serverhopping, HHUB will turn off every toggle to not get caught

</details>

<details>
<summary><b>#12 — Word Logger</b></summary>

- logs every word for you, even words that are not present in the word list
- `Clear History` clears the word history
- `Copy History` copies every soundid and word in the dropdown to your clipboard
- `Export History` exports the word history to a txt file in your executors workspace folder for you to read
- `Copy Word` copies the selected word in the dropdown
- `Copy SoundId` copies the selected words' soundid if found
- `Play Sound` plays the currently selected words' soundid

</details>

<details>
<summary><b>#13 — Player Mods</b></summary>

- `Allow Rotation` allows you to rotate your character in-game without it facing forwards
- `Allow Movement` allows you to walk around without being pulled to any spot
  - both of these are blatant, however, so use only if you prefer being banned
   - (these features are NOT detected, but using it too much in a single game draws suspicion

</details>

<details>
<summary><b>#14 — Mini Mode</b></summary>

- creates a watermark near the top left corner of your screen, which shows the current word. this watermark is draggable, and made to use with the ui minimized so you can see the word in a smaller menu. mainly created for mobile users, but works on every device. highly recommended to use this

</details>
