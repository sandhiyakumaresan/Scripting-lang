class BankAccount
  attr_reader :balance

  # Initialize the account with an optional starting balance
  def initialize(initial_balance = 0)
    @balance = initial_balance
  end

  # Method to deposit money into the account
  def add_balance(amount)
    if amount > 0
      @balance += amount
      puts "Successfully deposited $#{amount}. Current balance: $#{@balance}."
    else
      puts "Error: Deposit amount must be greater than zero."
    end
  end

  # Method to withdraw money from the account
  def withdraw(amount)
    if amount <= @balance
      @balance -= amount
      puts "Successfully withdrew $#{amount}. Current balance: $#{@balance}."
    else
      puts "Error: Insufficient funds. Current balance: $#{@balance}."
    end
  end

  # Method to check the current balance
  def check_balance
    puts "Current balance: $#{@balance}."
  end
end

# Example usage:
account = BankAccount.new(100)  # Initialize with a starting balance of $100
account.add_balance(50)          # Deposit $50
account.withdraw(30)             # Withdraw $30
account.check_balance            # Check current balance
account.add_balance(-10)         # Try to deposit a negative amount (error)
