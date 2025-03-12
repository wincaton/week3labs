# Instructor-led Lab

In this assignment you will create a Python notebook showcasing the concepts you learned about in the tutorial.

## Celsius and Fahrenheit Conversion (again)

In this assignment you will revisit your Celsius-to-Fahrenheit converter program. Go ahead and copy the contents of your last Python file into this assignment. For this assignment, you will be using the various operators to compare inputs and calculated values. Additionally, you will introduce the temperature scale Kelvin.

## Kelvin Temperature Scale

The conversion from Kelvin to Celsius is more straight forward than converting Celsius to Fahrenheit. The equation is

> Celsius = Kelvin - 273.15

In your notebook, perform the following:

* Add a variable to assign the value for Kelvin
* Write code to convert Celsius to Kelvin; this should occur after your code converts Celsius to Fahrenheit.
* Where you output the values for Celsius and Fahrenheit, add Kelvin too. Your output should look like this:

> *c* degrees Celsius is *f* degrees Fahrenheit which is *k* degrees Kelvin.

## Comparison Operators

Now that your program is able to generate values for Kelvin, you will further extend the program to compare your temperature values to a second set of temperature values. 

### Second Set of Variables 

You will need to create three new variables: `celsius_two`, `fahrenheit_two`, and `kelvin_two`. You will prompt the user for input (i.e., celsius) like you did above and convert it into Fahrenheit and Kelvin. In a code cell, output the new values, similar to what you did previously, only with a slight modification like so: 

> Second set of values: *c* degrees Celsius is *f* degrees Fahrenheit which is *k* degrees Kelvin.

### Comparison of Variables

You will compare the values generated for each of the new temperature variables using the operators in the table below to the original set of temperature values. Thus, you will have three pairs of values to compare.

| Operator | Name | Example |
|:---|:---|:---|
| `==` | Equal to | `x == y` |
| `!=` | Not equal to | `x != y` |
| `>`| Greater than | `x > y` |
| `<`| Less than | `x < y` |
| `>=` | Greater than or equal to | `x >= y` |
| `<=` | Less than or equal to | `x <= y` |

Create code that compares the Celsius values, the Fahrenheit values, and the Kelvin values. The comparison operator is preselected by you, but you should use a variety for all your comparisons. For each comparison, you will output text based on the result of the comparison. You will need to use a combination of `if` and `elif` statements.

For example, here is a table that provides some of the logic I might use for my program:

| Comparison | Result | Text |
|:---:|:---:|:---|
| celsius > celsius_two | Original value is larger | "The original Celsius value of {value} is larger than the new value of {value}." |
| celsius < celsius_two | New value is larger | "The original Celsius value of {value} is smaller than the new value of {value}." |
| celsius == celsius_two | Both are equal | "The original Celsius value of {value} equals the new value of {value}." |
| fahrenheit >= fahrenheit_two | Original value is larger | "The original Fahrenheit value of {value} is greater than or equal to the new value of {value}." |
| fahrenheit < fahrenheit_two | New value is larger | "The original Fahrenheit value of {value} is smaller than the new value of {value}." |
| fahrenheit == fahrenheit_two | Both are equal | "The original Fahrenheit value of {value} is equal to {value}." |
| kelvin <= kelvin_two | Original value is larger | "The original Kelvin value of {value} is less than or equal to the new value of {value}." |
| kelvin < kelvin_two | New value is larger | "The original Kelvin value of {value} is smaller than the new value of {value}." |
| kelvin != kelvin_two | Not equal | "The original Kelvin value of {value} is not equal to the new value of {value}." |

For example, if I type `-40` for my first value of celsius and then type in `0` for my second value, the following will output:

```
Welcome to my Fahrenheit to Celsius converter!
Please provide a value, in Celsius, to convert:
-40
-40.0 degrees Celsius is -40.0 degrees Fahrenheit which is 233.14999999999998 degrees Kelvin.

Please provide another value, in Celsius, to convert:       
0
Second set of values: 0.0 degrees Celsius is 32.0 degrees Fahrenheit which is 273.15 degrees Kelvin.

The original Celsius value of -40.0 is smaller than the new value of 0.0.
The original Fahrenheit value of -40.0 is smaller than the new value of 32.0.
The original Kelvin value of 233.14999999999998 is less than or equal to the new value of 273.15.
```

If I choose `80` and `-10` as my new set of Celsius values, the following is output:

```
Welcome to my Fahrenheit to Celsius converter!
Please provide a value, in Celsius, to convert:
80
80.0 degrees Celsius is 176.0 degrees Fahrenheit which is 353.15 degrees Kelvin.

Please provide another value, in Celsius, to convert:       
-10
Second set of values: -10.0 degrees Celsius is 14.0 degrees Fahrenheit which is 263.15 degrees Kelvin.

The original Celsius value of 80.0 is larger than the new value of -10.0.
The original Fahrenheit value of 176.0 is greater than or equal to the new value of 14.0.
The original Kelvin value of 353.15 is not equal to the new value of 263.15.
```

## Logical Operators

Let's extend your program one more time. We are going to use the logical operators `and` and `or`. 

You will use one of your Celsius comparisons and one of your Fahrenheit comparisons with the `and` logical operator to evalute both and output the results. If both are true, output, "Python speaks the truth!" If it is not, ouput, "Python lies." Prior to your comparison, please print to the screen what your comparison is.

Using one of your Celsius comparisons and one of your Kelvin comparisons from above, use the `or` logical operator. Provide the same output. Prior to your comparison, please print to the screen what your comparison is.

Here is an example of my output:

```
Welcome to my Fahrenheit to Celsius converter!
Please provide a value, in Celsius, to convert:
-40
-40.0 degrees Celsius is -40.0 degrees Fahrenheit which is 233.14999999999998 degrees Kelvin.

Please provide another value, in Celsius, to convert:       
0
Second set of values: 0.0 degrees Celsius is 32.0 degrees Fahrenheit which is 273.15 degrees Kelvin.

The original Celsius value of -40.0 is smaller than the new value of 0.0.
The original Fahrenheit value of -40.0 is smaller than the new value of 32.0.
The original Kelvin value of 233.14999999999998 is less than or equal to the new value of 273.15.

celsius == celsius_two and fahrenheit < fahrenheit_two        
Python lies.

celsius == celsius_two or kelvin != kelvin_two
Python speaks the truth!
```
