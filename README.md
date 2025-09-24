# Week 3 Python Assignment  
## Discount Calculator Program  

### Assignment Description  
Create a function named **`calculate_discount(price, discount_percent)`** that calculates the final price after applying a discount.  

- The function should take the original price (`price`) and the discount percentage (`discount_percent`) as parameters.  
- If the discount is **20% or higher**, apply the discount.  
- Otherwise, return the original price.  

Using the `calculate_discount` function, prompt the user to enter:  
1. The original price of an item.  
2. The discount percentage.  

Finally, print the final price after applying the discount, or if no discount was applied, print the original price.  

---

### Code Implementation  

```python
def calculate_discount(price, discount_percent):
    """
    Calculate the final price after applying discount.
    If discount is less than 20%, return the original price.
    """
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price


# Main program
# Prompt user for input
price = float(input("Enter the original price: "))
discount_percent = float(input("Enter the discount percentage: "))

# Call the function
final_price = calculate_discount(price, discount_percent)

# Display the result
if discount_percent >= 20:
    print(f"Final price after {discount_percent}% discount: {final_price:.2f}")
else:
    print(f"No discount applied. Final price: {final_price:.2f}")
