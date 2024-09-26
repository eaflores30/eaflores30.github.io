```mermaid
flowchart TD
 A(Start)
 B(Generate new random number variable from 1 to 10)
 C(Request new user input)
 D(Validate user input)
 E(Compare user input to number variable)
 F(Return that user input was Too Low)
 G(Return that user input was Correct)
 H(Return that user input was Too High)
 I(End)

 A --> B
 B --> C
 C --> D
 D - User input non-numeric or out of range -> C
 D --> E
 E - markdown["`User input < number variable`"] -> F
 E - markdown["`User input == number variable`"] -> G
 E - markdown["`User input > number variable`"] -> H
 F & H --> C
 G --> I
```
#### Documentation
After starting the program, a random number in the range 1-10 is generated and stored in a variable. Next, the program requests an input from the user. The program validates the input to ensure that it is both numeric and in the range of 1-10. If it is not, the program requests a new user input and revalidates. If it is valid, the program compares the input to the variable of the randomly generated number. If the input is less or greater than that of the randomly generated number, the program provides the according feedback and requests new user input. If the input is equal to the randomly generated number, the program informs that the user was correct and ends.