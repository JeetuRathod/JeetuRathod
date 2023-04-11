//Guess The Number Game!
import java.util.*;
public class GuessNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Random rm = new Random();
        int number = rm.nextInt(50)+1; //Guess number from 1 to 50 as random
        //Array to store guesses
        int Guesses[] = new int[10];
        //initialize guesses
        int numGuesses = 0;
        System.out.println("I am Thinking Number from 1 to 10 Can you guess it?");
        while (numGuesses < 10) { //Can Guess upto 10 times
            System.out.print("Enter Your Guesses: ");
            int Guess = sc.nextInt();
            Guesses[numGuesses] = Guess; //Add User Guess To the array
            numGuesses++;
            if (Guess == number) {
                System.out.println("Congratulations You Guessed Right number!");
                break;
            }else if(Guess > number){
                System.out.println("To High ");
            }else{
                System.out.println("TO Low Guess");
            }
        }
        if (numGuesses == 10) { //If guesses reached upto 10
            System.out.println("Sorry you didn't guess right number! The number was "+ number+".");
        }
        //Display the guesses Numbers
        System.out.print("Your Guesses Are: ");
        for (int i = 0; i < Guesses.length; i++) {
            System.out.print(Guesses[i]+" ");
        }
    }
}
