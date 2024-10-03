flowchart TD
    Start([Start]) --> RandomNumberGeneration
    RandomNumberGeneration[Generate random number (1-100)] --> UserInputValidation
    UserInputValidation{Is user input valid?} -->|No| InvalidInput[Display error message]
    InvalidInput --> UserInputValidation
    UserInputValidation -->|Yes| CheckGuess
    CheckGuess[Check if guess is correct] -->|Correct| CorrectGuess[Display "Correct!"]
    CheckGuess -->|Too High| HighGuess[Display "Too high! Try again."]
    CheckGuess -->|Too Low| LowGuess[Display "Too low! Try again."]
    HighGuess --> UserInputValidation
    LowGuess --> UserInputValidation
    CorrectGuess --> End([End])