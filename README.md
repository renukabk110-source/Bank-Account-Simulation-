# Bank-Account-Simulation-
class BankAccount {

   private String accountHolder;
    private double balance;
    public BankAccount(String name, double initialBalance) {
        accountHolder = name;
        balance = initialBalance;
    }
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: " + amount);
        } else {
            System.out.println("Invalid deposit amount!");
        }
    }
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn: " + amount);
        } else {
            System.out.println("Insufficient balance or invalid amount!");
        }
    }
    public void checkBalance() {
        System.out.println("Current Balance: " + balance);
    }
}
