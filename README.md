# guess
Game
 I am created a program in java in which the computer randomly guesses a number between 1-50 and allows the user to guess to the number. 
If the number is lower than the random number the program should say: lower! And of higher, the program should say: higher! If the user guesses the right number it should says ‘Yes’ you guessed the right number in correct(Yes) amount of tries.


package test;

import java.util.Scanner;
import java.util.logging.Logger;
import java.util.Random;

public class test {

public static void main(String[] args) {
	

    Random generator = new Random();
    Scanner reader = new Scanner(System.in);

    String higher = "higher", lower = "lower", correct = "Yes", input;
    int guess, random, random2 = 1, random3 = 50, randomLast, cntr = 1;

    random = generator.nextInt(50) + 1;
    randomLast = random;
    System.out.println("Is your number: " + random);
    System.out.println("Computer: Is the number should be higher, lower, or Yes: ");
    input = reader.next();

    while (!input.equals("Yes")){
        if (input.equals("lower")){
            randomLast = random2;
            random2 = generator.nextInt(50) + 1;
            if ((random2 < random) && (random2 < randomLast)){
            random = random2;
            cntr += 1;
            System.out.println("Is your number: " + random);
            System.out.println("Computer: Is the number should be higher, lower, or Yes: ");
            input = reader.next();
            } else {
                input = lower;
            }
        } else if (input.equals("higher")){
            randomLast = random3;
            random3 = generator.nextInt(50) + 1;
            if ((random3 > random) && (random3 > randomLast)){
            random = random3;
            cntr += 1;
            System.out.println("Is your number: " + random);
            System.out.println("Computer: Is the number  should be higher, lower, or Yes: ");
            input = reader.next();
            } else {
                input = higher;
            }
        }

    }

    System.out.println("Computer took " + cntr + " amount of tries to guess your number");

    }

	
}



Out Put:

Computer: Is the number  should be higher, lower, or Yes: 
higher
Is your number: 43
Computer: Is the number  should be higher, lower, or Yes: 
higher
Is your number: 47
Computer: Is the number  should be higher, lower, or Yes: 
higher
Is your number: 49
Computer: Is the number  should be higher, lower, or Yes: 
higher
Is your number: 50
Computer: Is the number  should be higher, lower, or Yes: 
yes

 
