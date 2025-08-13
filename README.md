# Week3-python-assignment
🛒 Discount Calculator
This is a simple Python program that calculates the final price of an item after applying a discount.
If the discount is 20% or higher, it applies the discount; otherwise, it returns the original price.

📜 Features
Takes original price and discount percentage as input.

Applies discount only if it is ≥ 20%.

Displays final price or original price depending on the discount.

Handles invalid inputs gracefully.

🖥 Example Usage
bash
Copy
Edit
Enter the original price of the item: 1000
Enter the discount percentage: 25
Final price after 25.0% discount: $750.00
bash
Copy
Edit
Enter the original price of the item: 500
Enter the discount percentage: 15
No discount applied. Price remains: $500.00
📂 Code
python
Copy
Edit
def calculate_discount(price, discount_percent):
    # Check if discount is 20% or more
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Prompt the user for input
try:
    price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))

    final_price = calculate_discount(price, discount_percent)

    # Print result
    if discount_percent >= 20:
        print(f"Final price after {discount_percent}% discount: ${final_price:.2f}")
    else:
        print(f"No discount applied. Price remains: ${final_price:.2f}")
except ValueError:
    print("Invalid input. Please enter numeric values for price and discount.")
🚀 How to Run
Clone this repository

bash
Copy
Edit
git clone https://github.com/Charley-sys/Week3-python-assignment.git
cd discount-calculator
Run the Python script

