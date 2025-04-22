# Week_5-Kabaka-dev

1. Create a function named calculate_discount(price, discount_percent) that calculates the final price after applying a discount. The function should take the original price (price) and the discount percentage (discount_percent) as parameters. If the discount is 20% or higher, apply the discount; otherwise, return the original price.
2. Using the calculate_discount function, prompt the user to enter the original price of an item and the discount percentage. Print the final price after applying the discount, or if no discount was applied, print the original price.

def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount if applicable.
    
    Parameters:
    price (float): Original price of the item
    discount_percent (float): Discount percentage (0-100)
    
    Returns:
    float: Final price after discount (or original price if discount < 20%)
    """
    if discount_percent >= 20:
        discounted_price = price * (1 - discount_percent / 100)
        return discounted_price
    else:
        return price

# Get user input
original_price = float(input("Enter the original price of the item: "))
discount = float(input("Enter the discount percentage (0-100): "))

# Calculate and display the final price
final_price = calculate_discount(original_price, discount)

if discount >= 20:
    print(f"After applying a {discount}% discount, the final price is: ${final_price:.2f}")
else:
    print(f"No discount applied. The original price is: ${original_price:.2f}")
