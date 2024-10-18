# Guessing Game
### ZZZ characters

``` mermaid
flowchart TD

A(Start) --> B[Call Intro Function<br> Set attempt variable: 3]
B --> C[Print Hello! Welcome to the ZZZ guessing game!]
C --> D[/Ready to<br>start game?/]
D --> |Yes!| E[Start Game Function]
E --> H[Randomly pick index num of zzz character in list]
H --> I[Print List of zzz characters with index num]
I --> J[/Guess what <br>zzz character<br> I picked:/]
J --> |User inputs num| K{Is inputed num <br>= <br>selected num?}
K --> |Yes!| M[Print Correct! Next Question]
M --> H
K --> |No!| L[Print Wrong! Try again. Answer is ___ away. <br>attempts -1]
L --> W{Is attempt = 0?}
W --> |Yes| F
W --> |No| I
D --> |No!| F[Call End Function]
F --> Z[Print Goodbye!<br> Thank you for,<br> playing my game!]
Z --> X(End)

```
## Documentation
Starting game Input: Asks user if they are ready to start the game. Yes? Start Game Function. No? Start End Function
### Intro Function
Setting variable attempt: 
<br>This variable tracks the amount of attempts the user had before sending to the end function

Printed output: 
<br>Welcomes the user to the game
### Game Function
Picking zzz Character:
<br>Randomly select a character in a list and get its index num

User input:
<br>Display the list of zzz characters and their index num. Ask user to input an index num for their selected 

Comparing inputed num and selected num:Are both the same?
<br>Yes, Print Correct. No, Print Wrong and decrease attempt by 1.
<br>Shows how far the user's answer is to the right answer.

Checking attempt variable:
<br>Is attempt = 0? Yes, start end function. No, pass

### End Function
 Printed Output:
<br>Thanks the user for playing my game.

