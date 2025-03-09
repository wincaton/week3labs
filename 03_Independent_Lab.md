# Independent Lab

In this assignment you will create a Python notebook showcasing the concepts you learned about in the tutorial.


## Self-Service Kiosk Logic Logic

In this assignment you will build logic for a self-service kiosk. While the logic for an actual kiosk machine is a little more complex than what you will create, in essence, your program will capture the foundational aspects. This includes product selection, quantity, pricing, and payment.

Assume the following aspects about your kiosk:

* It sells 5 different products, your choice.
  * Each product has its own price.
  * While two products can have the same listed price, the variables should be different. Display the prices to the user along with the product names using string interpolation.
  * The names of the products and their prices should come from variables. Thus, you will have a total of 5 variables for product names, 5 variables for prices.
* Your program will prompt the user to select a product. It will then prompt them to enter the quantity desired.
  * Confirm what the customer selected and the quantity by outputting the product and quantity to the screen using string interpolation.
* The user can select multiple products with multiple quantities.
  * Additionally, the user can repeat a product order (i.e., the user places an order for 3 pizzas and then decides to add 2 more).
* The user is given the total cost of their order after each selection.
* The program should prompt the user when to complete (i.e., end) their order.
  * The program will confirm which items the customer has ordered along with the quantity.
  * The user *is also given* the total at the completion of their order.
* Your `if-else` statement must have a default or fall-back option that captures any incorrect input from the user. This statement will output, "That is not an option. Please try again."

Your program will need to rely on an infinite loop to continuously provide the user access to the menu selection prompt. This means that when the customer completes their order, you will need to implement a jump statement that ends the infinite loop.

Also, keep in mind that when your program reads in user input, it is stored as a string. So, even if a user enters a number, that number is stored as a string, not an integer or float.

Below is an example from the key of what your program may look like. I created a table to display the products to the customer; *you do not need to recreate it*. I just wanted to display the information in a nicely formatted package.

Start of kiosk order:

```
Welcome! This kiosk sells tickets and passes for your local ski resort.
Please place your order by selecting the product and subsequently providing the quantity desired.

Here are the ticket options:

|   | Product                        | Price   |
| 1 | Single Day Ticket - Weekday    | $50.00  |
| 2 | Single Day Ticket - Weekend    | $78.00  |
| 3 | Season Pass - Adult            | $469.00 |
| 4 | Season Pass - Child            | $259.00 |
| 5 | Season Pass - Senior           | $459.00 |


What would you like to purchase?
1

How many would you like to purchase?
3

You want 3 of Single Day Ticket - Specific Date.

The current total for your order is $150.00
```

Continuation of kiosk order. Customer selects additional prodcuts:

```
You want 3 of Single Day Ticket - Specific Date.

The current total for your order is $150.00

If you are finished ordering, please input 1; otherwise, if you would like to add to your order, please input 2.
2

Adding to your order...


What would you like to order?
4

How many would you like to order?
1

You want 1 of Season Pass - Child.

The current total for your order is $609.00

If you are finished ordering, please input 1; otherwise, if you would like to add to your order, please input 2.
1
```

The order is complete and a summary is displayed:

```
The current total for your order is $609.00

If you are finished ordering, please input 1; otherwise, if you would like to add to your order, please input 2.
1

Here is a summary of your final order:

| Product                        | Quantity |
| Single Day Ticket - Weekday    |     3    |
| Single Day Ticket - Weekend    |     0    |
| Season Pass - Adult            |     0    |
| Season Pass - Child            |     1    |
| Season Pass - Senior           |     0    |

The total cost for your order is $609.00
```