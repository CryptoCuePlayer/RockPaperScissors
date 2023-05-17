# RockPaperScissors
RockPaperScissors
import java.util.Scanner;

public class RockPaperScissors {
    public static void playGame() {
        String[] choices = {"камень", "ножницы", "бумага"};

        Scanner scanner = new Scanner(System.in);
        System.out.println("Введите свой выбор (камень, ножницы или бумага):");
        String userChoice = scanner.nextLine().toLowerCase();

        if (!userChoice.equals("камень") && !userChoice.equals("ножницы") && !userChoice.equals("бумага")) {
            System.out.println("Некорректный выбор. Попробуйте снова.");
            playGame();
        } else {
            int computerChoiceIndex = (int) (Math.random() * choices.length);
            String computerChoice = choices[computerChoiceIndex];

            System.out.println("Компьютер выбрал: " + computerChoice);

            if (userChoice.equals(computerChoice)) {
                System.out.println("Ничья!");
            } else if ((userChoice.equals("камень") && computerChoice.equals("ножницы")) ||
                    (userChoice.equals("ножницы") && computerChoice.equals("бумага")) ||
                    (userChoice.equals("бумага") && computerChoice.equals("камень"))) {
                System.out.println("Вы победили!");
            } else {
                System.out.println("Вы проиграли!");
            }
        }
    }

    public static void main(String[] args) {
        System.out.println("Игра \"Камень, ножницы, бумага\" начинается!");
        playGame();
    }
}
