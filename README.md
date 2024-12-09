# OasisInternship_JP
import java.util.Scanner;

//<<<<<<<ATM INTERFACE>>>>>>>>>>
class CodSoft {
    public static void main(String args[]) {
        System.out.println("_______WELCOME TO MY ATM MACHINE!!_________");
        Scanner sc = new Scanner(System.in);
        int balance = 80000, deposite, withdraw, transfer;
        while (true) {
            System.out.println("1.choose 1 for deposite the money");
            System.out.println("2.choose 2 for withdraw the money");
            System.out.println("3.choose 3 for transfer the money");
            System.out.println("4.choose 4 for checking transaction history");
            System.out.println("5.choose 5 for quit!!");
            System.out.println("choose any number for operation=");

            int choice = sc.nextInt();
            switch (choice) {
                case 1:
                    System.out.println("Enter your money to deposite= ");
                    deposite = sc.nextInt();
                    balance += deposite; //balance=balance+deposite
                    System.out.println("Your money is deposited successfully!!");
                    System.out.println("The updated balace is:" + balance);
                    break;
                case 2:
                    System.out.println("Enter your money to withdraw=");
                    withdraw = sc.nextInt();
                    if (balance >= withdraw) {
                        balance -= withdraw; //balance=balance-withdraw
                        System.out.println("Your money is withdrawed successfully!!");
                        System.out.println("The updated balance is:" + balance);
                    } else {
                        System.out.println("oops!! Insufficient balance");
                    }
                    break;
                case 3:
                    System.out.println("Enter your money to transfer=");
                    transfer = sc.nextInt();
                    if (balance >= transfer) {
                        balance -= transfer; //balance=balance-transfer
                        System.out.println("Enter your pin=");
                        int pin = sc.nextInt();
                        if (pin == 5151) {
                            System.out.print("Your money has been transferred successfully!!");
                            System.out.println("Your updated balnce is:" + balance);

                        } else {
                            System.out.println("Pin is incorrect!!");
                        }
                    }
                    break;
                case 4:
                    System.out.println("Enter your pin to check transaction history=");
                    int pin = sc.nextInt();
                    if (pin == 9191) {
                        System.out.println("The recent transactions are:");
                        System.out.println("money deposited=" + 1000);
                        System.out.println("money withdrawed=" + 10000);
                        System.out.println("money transferred=" + 5000);
                    } else {
                        System.out.println("The pin is incorrect!");
                    }
                    break;
                case 5:
                    System.out.println("________CLOSING THE ATM!!___________");
                    System.exit(0);

            }
        }
    }
}
