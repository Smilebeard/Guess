```mermaid
flowchart TD
Start([Start]) --> End([End]

flowchart TD
    Start([Start]) --> |"A number is generated between 1-20"| GuessNumber
    GuessNumber -->|Is the guess correct?| CorrectAnswer{Is guess correct?}
    
    CorrectAnswer -->|Yes| Congrats([You got it])
    CorrectAnswer -->|No| CheckHigherOrLower{Is the guess higher or lower than the number?}
    
    CheckHigherOrLower -->|Higher| GuessLower([Too high, try a lower number.])
    CheckHigherOrLower -->|Lower| GuessHigher([Too low, try a higher number.])
    
    GuessLower --> GuessNumber
    GuessHigher --> GuessNumber

The chart starts out on line 6 with a random number between 1-20 being generated and then the user trying to guess it.
It then brances into two seperate forks that are does the user guess correctly or not. If correct it will display "you got it" and the flowchart ends. If the number is incorrect it will then inform you if your guess is too low or high and prompt you to guess again until your guess is correct.
