## Simple Term

### Code Details

1. **Microcontroller Compatibility**: ????.
2. **LCD Connection**: Utilizes an I2C LCD 2004 display.
3. **Indicators**: Equipped with one or more LEDs for status indication.
4. **Keypad**: Features a 10-button keypad plus 2 additional buttons.
5. **Audio Feedback**: Includes a buzzer for sound alerts.
6. **Storage**: Connected to a memory card module.
7. **Audio Output**: Connected to a speaker module via I2S.

### Use Case

1. **Welcome Menu**:
    - The device welcomes the user and prompts them to choose an action:
        a. Listening
        b. Answering

2. **Listening Mode**:
    - Selection is made using the 2 dedicated buttons.
    - Confirmation prompt: "Are you sure?" (Options: Yes/No).
    - If confirmed, the user is prompted to enter the file number using the 10-button keypad.
    - Confirmation is required before playing the sound.
    - Use the dedicated buttons for actions like delete/enter.
    - Cancel/Return functionality allows the user to go back to the previous step.

3. **Answering Mode**:
    - A random file is played, and the user is prompted to guess the file number.
    - Correct guess: +1 score.
    - Incorrect guess: -1 score.
    - The game exits when the score reaches 0 (Game Over) or 10 (Victory).
    - Exit or continue options are available using the 2 dedicated buttons. Initial score is set at 5.

## In Detailed Term

### Detailed Code Requirements

#### Hardware Components

1. **Microcontroller**:
   - To be discuss.

2. **Display**:
   - 2004 I2C LCD Display (20 characters by 4 lines).

3. **Indicators**:
   - One or more LEDs to indicate different statuses (e.g., power on, operation mode).

4. **Keypad**:
   - A 10-button numeric keypad for user input (buttons labeled 0-9).
   - Two additional buttons for navigation (labeled Enter and Delete).

5. **Audio Feedback**:
   - A buzzer for auditory alerts.

6. **Storage**:
   - A memory card module for storing audio files.

7. **Audio Output**:
   - A speaker module connected via I2S for playing sound.

#### Functional Requirements

##### Welcome Menu

1. **Initial Prompt**:
   - Upon startup, the device displays a welcome message on the LCD and asks the user to choose an action:
     - a. Listening
     - b. Answering

2. **Selection Process**:
   - The user selects an option using the two dedicated buttons (Enter and Delete).

##### Listening Mode

1. **Confirmation**:
   - After selecting "Listening", the device asks for confirmation: "Are you sure? (Yes/No)".
   - User confirms using the dedicated buttons.

2. **File Selection**:
   - Upon confirmation, the device prompts the user to enter a file number using the 10-button keypad.
   - The user can enter the number and confirm with the Enter button.

3. **Play Audio**:
   - The device asks for another confirmation before playing the sound: "Play file X? (Yes/No)".
   - If confirmed, the sound file corresponding to the entered number is played through the speaker.

4. **Navigation**:
   - The user can cancel and return to the previous step at any point using the Delete button.

##### Answering Mode

1. **Game Start**:
   - The device randomly selects and plays an audio file.
   - The user is prompted to guess the file number by entering it using the 10-button keypad.

2. **Scoring**:
   - If the guess is correct, the user’s score increases by 1.
   - If the guess is incorrect, the user’s score decreases by 1.
   - The initial score is set to 5.

3. **End Conditions**:
   - The game ends if the user's score reaches 0 (Game Over) or 10 (Victory).
   - The device provides the option to exit or continue the game using the dedicated buttons.

4. **Navigation**:
   - The user can exit the game at any time using the two dedicated buttons (Exit/Continue).

#### User Interaction Flow

1. **Startup**:
   - Display: "Welcome! What would you like to do?"
   - Options: "a. Listening b. Answering"

2. **Listening Mode**:
   - Display: "Are you sure? (Yes/No)"
   - If Yes: "Enter file number:"
   - After entry: "Play file X? (Yes/No)"
   - If Yes: Play sound file.
   - Use Delete to cancel and return to the previous step.

3. **Answering Mode**:
   - Play random audio file.
   - Display: "Guess the file number:"
   - After guess: "Correct!" or "Incorrect!"
   - Update score: "Score: X"
   - End game conditions: "Game Over" or "Victory!"
   - Option to exit or continue.

### Additional Considerations

- **Error Handling**:
  - Display appropriate error messages for invalid inputs or file not found.

- **Power Management**:
  - Ensure efficient power usage to prolong battery life if the device is portable.

- **User Feedback**:
  - Use LEDs and buzzer to provide additional feedback for user actions (e.g., input accepted, error).

- **Memory Management**:
  - Efficiently manage memory card storage and retrieval to handle multiple audio files.

