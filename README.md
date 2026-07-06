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

        String[] playerHand = {"","✊", "✋", "✌\uFE0F"};
        String[] BotHand = {"","✊","✋","✌\uFE0F"};


        if(pick == enemypick) {
            System.out.println("You: " + playerHand[pick] + " VS " + BotHand[enemypick] + ":Bot");
            System.out.print("Tie");
        }
        else if((pick == 1 && enemypick == 2) || (pick == 2 && enemypick == 3) || (pick == 3 && enemypick == 1)){
                System.out.println("You: " + playerHand[pick] + " VS " + BotHand[enemypick] + ":Bot");
                System.out.println("===========================");

                System.out.print("         You Lose");
        }
        else{
            System.out.println("You: " + playerHand[pick] + " VS " + BotHand[enemypick] + ":Bot");
            System.out.println("===========================");

            System.out.print("         You Win");
        }
        scanner.close();
    }
}
