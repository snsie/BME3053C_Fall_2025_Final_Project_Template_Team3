# BioWordle

BioWordle is a browser-based word game where players guess 5-letter Biomedical terms, making it easy and fun for students to review Biomedical concepts. 

## Biomedical Context

BioWordle is designed for undergraduate biomedical engineering and pre-med students who want to reinforce key terminology related to human physiology, medical devices, and biomedical signals. By repeatedly guessing category-specific words, players are exposed to common anatomical structures, tools, and signal-processing terms, helping them build familiarity with professional vocabulary used in coursework and clinical settings.

## Quick Start Instructions
How to Open the Repo in GitHub Codespaces:
1. Go to the project repository on GitHub.
2. Click the green Code button.
3. Select the Codespaces tab.
4. Click Create codespace on main (or reopen an existing codespace if one already exists).
5. Wait for the Codespace to finish building and for the VS Code environment to open in the browser.
### Opening the Repository in GitHub Codespaces

### Running the Application

1. In the terminal in Codespaces, run the following command to go into the correct folder: cd game
2. Then type "DISPLAY=:0 love ." to start running the game.
3. In the bottom panel, click the "Ports" tab.
4. Find the port that was created for the VNC view and click the globe icon next to its URL (it says “Open in browser” on hover). It should be on Port 6080.
5. In the browser tab that opens, click the last link titled "vnc_lite.html".

## Usage Guide

Step 1: Welcome Screen
- You will see a “Welcome to BioWordle!” message and a brief description.
- Press Enter or Space to continue to the category selection screen.
<img width="2879" height="1806" alt="image" src="https://github.com/user-attachments/assets/37981985-d6ad-4c1c-ab5a-360b54cc7775" />

Step 2: Choose a Category
- The next screen lists the three categories: physiology, devices, and signals.
- Click in the window so it has focus.
- Start typing the name of the category you want (e.g., physiology).
- Press Enter to confirm. Inputs starting with phys select physiology, dev selects devices, and sig selects signals. If the category is not recognized, an error message appears prompting you to use one of the valid names.
<img width="2890" height="1808" alt="image" src="https://github.com/user-attachments/assets/64fdc10e-37c9-4e64-b4d4-8afbd5cd6c1a" />

Step 3: PLaying a Round
Once a category is chosed, the main BioWordle grid appears:
- The top of the screen shows the game title and current category (e.g., “Category: physiology”).
- You have 6 rows of 5 tiles, each representing a guess at the secret five-letter word.
- Start typing letters on your keyboard. Letters appear in the current row from left to right. Use Backspace to delete the most recent letter.
- When the row is full (5 letters), press Enter to submit your guess.
<img width="776" height="613" alt="image" src="https://github.com/user-attachments/assets/12897213-f473-434e-8c1a-c3a67f395035" />

Step 4: Tile Colors & Feedback
After each submitted guess, tiles are colored using Wordle-style feedback:
- Green – The letter is in the correct position.
- Yellow – The letter is in the word but in a different position.
- Gray – The letter is not in the word (or all of that letter’s instances are already accounted for).

Use these hints to refine your next guess. All category words are valid biomedical terms from the selected category, so think in terms of anatomy, devices, or signal-related vocabulary.
<img width="2885" height="1808" alt="image" src="https://github.com/user-attachments/assets/a26c5b79-1ce7-4de3-a11c-1e4d20a8c31c" />

Step 5: Winning, Losing, & Restarting
- If you guess the word correctly within six tries, a congratulatory message appears (e.g., “Congratulations you guessed the word!”).
- If you use all six rows without finding the word, the game displays “Out of guesses. The word was: "HEART” (example).
- After the game is over: Press Enter or Space to return to the welcome screen. From there, you can start another round and choose the same or a different category.
<img width="2873" height="1803" alt="image" src="https://github.com/user-attachments/assets/c4b2f70e-d5d4-4cf2-a7ea-4145cacec726" />

## Project Structure
Below is an outline of the main files relevant to the BioWordle game (paths may be relative to the game folder in the template repo). There are two relevant files that are in a folder titled "game".

game/main.lua
- Core Love2D game file.
- Implements welcome screen, category selection, input handling, Wordle-style evaluation, tile coloring, win/lose logic, and drawing of the game grid. 

game/words.lua
- Contains the three word banks: physiology_words, device_words, and signal_words, each defined as a Lua table of uppercase five-letter terms. 

Final Project Report.pdf
- Written report describing the motivation, methods, experiments, user feedback, and proposed future improvements for BioWordle (e.g., longer words, more categories, larger fonts). 

README.md
- This document. Provides context, setup instructions, usage details, and a project overview.

Additional template files (e.g., devcontainer configuration, GitHub workflow files, etc.) come from the course’s final project template and help ensure reproducible execution in GitHub Codespaces.

