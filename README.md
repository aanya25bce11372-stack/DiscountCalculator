#Discount Calculator for Online Sales

def calculate_discount(amount, discount_percent):
    """Calculate discount amount and final price."""
    discount_amount = amount * discount_percent / 100
    final_price = amount - discount_amount
    return discount_amount, final_price
def main():
    print("=== Online Sales Discount Calculator ===")

    #Step 1: Get user input
    try:
        amount = float(input("Enter order amount: "))
        discount_percent = float(input("Enter discount percentage: "))
    except ValueError:
        print("Error: Please enter numeric values only.")
        return

    #Step 2: Validate input
    if amount < 0:
        print("Error: Order amount cannot be negative.")
        return

    if discount_percent < 0 or discount_percent > 100:
        print("Error: Discount percentage must be between 0 and 100.")
        return

    #Step 3: Calculate discount and final price
    discount_amount, final_price = calculate_discount(amount, discount_percent)

    #Step 4: Display results
    print("\n--- Bill Summary ---")
    print(f"Original amount : {amount:.2f}")
    print(f"Discount ({discount_percent:.2f}%) : {discount_amount:.2f}")
    print(f"Final amount to pay : {final_price:.2f}")


#Program entry point
if __name__ == "__main__":
    main()
