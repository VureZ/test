[![Codacy Badge](https://app.codacy.com/project/badge/Grade/dbfb76df49e2493a9cea3f95f5be863e)](https://app.codacy.com/gh/VureZ/test/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade)

public class BankAccount {
    private double balance = 0;
    private final String accountNumber;

    public BankAccount(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    public void deposit(double amount) {
        if(amount > 0) {
            balance += amount;
        } else {
            System.out.println("Deposit amount must be positive");
        }
    }

    public void withdraw(double amount) {
        if(amount > balance) {
            System.out.println("Insufficient balance");
            if(amount > balance) {
            System.out.println("Insufficient balance");
        } else {
            balance -= amount;
        }
    }

    public double getBalance() {
        return balance;
    }

    public String getAccountNumber() {
        return accountNumber;
    }
}

public class Bank {
    private final List<BankAccount> accounts;

    public Bank() {
        accounts = new ArrayList<>();
    }

    public void addAccount(String accountNumber) {
        accounts.add(new BankAccount(accountNumber));
    }

    public BankAccount getAccount(String accountNumber) {
        for(BankAccount account : accounts) {
            if(account.getAccountNumber().equals(accountNumber)) {
                return account;
            }
        }
        return null;
    }
}
