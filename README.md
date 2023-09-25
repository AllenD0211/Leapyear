import java.util.Scanner;

public class LeapYear {
	public static void main(String[] args) {
		Scanner input = new Scanner(System.in);
		int year;
		boolean tryAgain = true;

		while (tryAgain) {
			System.out.println("Enter a year: ");
			year = input.nextInt();

			if (isLeapYear(year)) {
				System.out.println(year + " is a leap year!");
			} else {
				System.out.println(year + " is not a leap year.");
			}

			System.out.print("Do you want to try again? (y/n) ");
			String answer = input.next();
			if (answer.toLowerCase().equals("n")) {
				tryAgain = false;
			}
		}
	}

	public static boolean isLeapYear(int year) {
		if (year % 4 == 0) {
			if (year % 100 == 0) {
				if (year % 400 == 0) {
					return true;
				} else {
					return false;
				}
			} else {
				return true;
			}
		} else {
			return false;
		}
	}
}
