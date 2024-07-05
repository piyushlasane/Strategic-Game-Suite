## Strategic Game Suite

### Code
```java
import java.util.Random;
import java.util.Scanner;

public class RockPaperScissor {
    public static void main(String[] args) {
        int user = 0, comp = 0;
        for (int i = 0; i < 3; i++) {
            Random r = new Random();
            int compInput = r.nextInt(1, 4);
            Scanner sc = new Scanner(System.in);
            System.out.print("Enter Your choice: ");
            int userInput = sc.nextInt();
            // 1 = Rock     2 = Paper     3 = Scissor
            if (compInput == userInput) {
                System.out.println("Match Draw");
            } else if ((compInput == 1 && userInput == 3) || (compInput == 2 && userInput == 1) || (compInput == 3 && userInput == 2)) {
                System.out.print("Computer Win, ");
                comp++;
            } else {
                System.out.print("You Win, ");
                user++;
            }
            System.out.println("Because Computer chose: " + compInput + " and You chose: " + userInput + "\n");
            sc.close();
        }
        System.out.println("Final Result: ");
        if (user < comp) {
            System.out.println("Computer win this Game!!");
        } else if (user > comp) {
            System.out.println("You win this Game!!");
        } else System.out.println("Match Draw");
    }
}
```
