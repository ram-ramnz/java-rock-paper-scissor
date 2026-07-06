import java.util.Scanner;
import java.util.Random;
public class Main{
    public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        System.out.println("======BATO BATO PICK!======");
        System.out.println("Pick a hand signal:");
        System.out.println("1).ROCK ✊");
        System.out.println("2).PAPER ✋");
        System.out.println("3).SCISSOR ✌\uFE0F");
        System.out.print("Pick: ");
        int pick = scanner.nextInt();
        int enemypick = random.nextInt(1,4);
        System.out.println("Bot: " + enemypick);
        System.out.println("===========================");

        if(pick < enemypick) {// you either 1 or 2
            if (pick < 2) { // you are rock
                if(enemypick == 3) {
                    System.out.println("You: ✊ vs ✌\uFE0F:Bot");
                    System.out.print("You Won");
                }
                else{
                    System.out.println("You: ✊ vs ✋:Bot");
                    System.out.print("You Lose");
                }
            }
            else {//you are paper
                if(enemypick == 3) {
                    System.out.println("You: ✋ vs ✌\uFE0F:Bot");
                    System.out.print("You Lose");
                }
                else{
                    System.out.println("You: ✋ vs ✊:Bot");
                    System.out.print("You Won");
                }
            }
        }
        else if(pick > enemypick) {//you either 2 or 3
            if(pick < 3){// you are paper
                if(enemypick == 3){
                    System.out.println("You: ✋ vs ✌\uFE0F:Bot");
                    System.out.print("You Lose");
                }
                else{
                    System.out.println("You: ✋ vs ✊:Bot");
                    System.out.print("You Won");
                }
            }
            else {
                if(enemypick == 1){//you are scissor
                    System.out.println("You: ✌\uFE0F vs ✊:Bot");
                    System.out.print("You Lose");
                }
                else{
                    System.out.println("You: ✌\uFE0F vs ✋:Bot");
                    System.out.print("You Won");
                }
            }
        }
        else{
            System.out.print("Tie");
            if(pick == 1){
                System.out.println("You: ✊ vs ✊ :Bot");
            }
            else if(pick == 2){
                System.out.println("You: ✋ vs ✋ :Bot");

            }
            else{
                System.out.println("You: ✌\uFE0F vs ✌\uFE0F :Bot");
            }
        }



        scanner.close();
    }
}****
