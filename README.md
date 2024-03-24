# linear_wave_function
A cos(x) wave function but the values increase/decrease linearly.

f(x)= (-1)^[[x]] * ([[x]] - x + (1/2))

**Note: I wrote this pretty late at night so there may be slight grammatical mistakes

The function f(x)=cos(x) starts from 1 and decreases at a non-constant rate before reaching x=pi (using radians) before beginning to increase at a non-constant rate until x=2*pi. 

The function I made produces a similar-looking output that has these properties:
1. A period of 2; P=2
2. Constant slope for each half-period and an undefined slope at x=P,(P/2); {-1, undefined, 1, undefined, -1, ...}
3. An amplitude of 1/2; A=1/2

I added an image of the graph from Desmos called example_graph1.png
**Note: Desmos uses the floor(x) function for the step function ( [[x]] ) but they do the same thing so that's why it appears like that in the example


# Modifying the function
Modifying the function in a couple of ways can produce different effects:

f(x)= a(-1)^[[bx]] * ([[cx]] - dx + (1/2)) + w

Modifying variable "a" changes A = (1/2) * a

Modifying variable "b"="c"="d" changes P = 2*b = 2*c = 2*d

Modifying variable w changes shifts the entire graph up or down by the value of w


The following are just interesting things I noticed:

Modifying variable "b" will create a dashed chain of rhombuses if b > 1

Modifying variable "b" will add linear lines halfway between each period if 0 < b < 1 and b is an Integer; the number of lines is equal to b^(-1) - 2 


# How the equation was made
The equation was made using 3 different equations put together:

h(x) = (-1)^[[x]]
g(x) = x - [[x]]
m(x) = (1 + (-1)^[[x]])/2
b(x) = -1/2

h(x) returns 1 if the [[x]] is even and -1 if [[x]] is odd
g(x) returns a pattern of linear segments (with a slope of 1) that approach y=1 before jumping to y=0 and repeating
m(x) returns 1 when x is even and 0 when x is odd **this is to fix the problem of discontinuity after h(x) and g(x) are multiplied together
b(x) is used to shift the graph down by 1/2

-1 * h(x) * g(x) = -1 * (-1)^[[x]] * (x - [[x]])      ***multiplied by -1 to make f(0) = 1 instead of f(0) = -1
-h(x)g(x)= (-1)^[[x]] * ([[x]] - x)

(-1)^[[x]] * ([[x]] - x) + m(x) + b(x) = (-1)^[[x]] * ([[x]] - x) + (1 + (-1)^[[x]])/2 + (-1/2)
= (-1)^[[x]] * ([[x]] - x) + (1 + (-1)^[[x]]) - 1) * 1/2   ***factor out 1/2
= (-1)^[[x]] * ([[x]] - x) + ((-1)^[[x]])) * 1/2
= (-1)^[[x]]) * ( ([[x]] - x) + (1/2) )     ***factor out (-1)^[[x]])
= (-1)^[[x]] * ([[x]] - x + (1/2))

f(x) = (-1)^[[x]] * ([[x]] - x + (1/2))

If there is anything that is unclear please let me know so I can fix it. Thank you.
