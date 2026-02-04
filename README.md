# Budget Grocery Shopping Cart 

A Python command-line application that simulates a grocery shopping experience while enforcing a user-defined budget.  
Users can add and remove items, apply random discounts, track remaining funds, and checkout—all powered by a CSV-based inventory.

## Overview

This project models a real-world shopping cart system where users must make purchasing decisions within a fixed budget.  
It reads grocery items and prices from a CSV file and allows users to interactively manage their cart through simple commands.

The goal of this project was to practice:
- Object-oriented programming in Python
- Working with external data using `pandas`
- Budget constraints and error handling
- Building a clean, interactive CLI experience

## Features

- Load grocery inventory from a CSV file
- Add items to a cart while staying within budget
- Automatically add unavailable items to a wishlist
- Remove items from the cart
- Apply a random coupon discount (5%–30%)
- View cart contents, total cost, and remaining budget
- Checkout with confirmation

## How to Use the Program

1. **Start the program**
   - Run the script from the project root:
     ```bash
     python src/shopping_cart.py
     ```

2. **Enter your budget**
   - You will be prompted to enter a dollar amount.
   - The program will not allow a budget less than or equal to zero.

3. **Add items to your cart**
   - Type the name of a grocery item exactly as it appears in the CSV file.
   - If the item exists and is within your budget, it will be added to your cart.
   - If the item is not found, it will be added to a wishlist.

4. **Use commands to manage your cart**
   - `view` → displays all items in your cart, total cost, and remaining budget
   - `remove` → prompts you to remove a specific item
   - `coupon` → applies a random discount between 5% and 30%
   - `checkout` → confirms your purchase and ends the program

5. **Checkout**
   - When you choose to checkout, the program shows a final summary.
   - You must confirm the purchase before the cart is cleared.

## How the Program Works (Behind the Scenes)

- Grocery items and prices are loaded from a CSV file using `pandas`.
- A `ShoppingCart` class manages:
  - the cart contents
  - the total price
  - the user’s remaining budget
- Each action (add, remove, coupon, checkout) updates the cart state in real time.
- Budget limits are enforced using error handling to prevent overspending.


