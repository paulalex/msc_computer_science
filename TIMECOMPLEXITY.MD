# Time complexity of Algorithms

In mathematical analysis, asymptotic analysis, also known as asymptotics, is a method of describing limiting behavior.


## Time Complexity Table



## Big-O

Big-O notation is used to classify algorithms based on the based on the number of operations or comparisons they use, typically big-O is used to the define the upper bounds, 
or worst case running time of a function. In plain words, Big O notation describes the complexity of your code using algebraic terms.

When we calculate big O notation, we only care about the dominant terms, and we do not care about the coefficients. Since we want to analyze the growth with respect to the input 
size, the coefficients which only multiply the number rather than growing with the input size do not contain useful information. The dominant term is the term that grows the fastest.

For large values of x: x², 3x² + 25, 4x² + 7x + 75 which are all similar we will treat them all as the same order O(x²).

**Big O**: f(n) is O(g(n)) if for some constants c and N₀, f(n) ≤ c * g(n) for all N > N₀

*What this means is that f(n) grows no faster that g(n).*

g(n) = n²
c = 1
N₀ = 0
n = 1000

Using the above values N² will always be greater than (N²/2) - (N/2)

n² = 1, 000, 000
(N²/2) - (N/2) = 499, 500

When we talk about Big O, we want to know the tight bound of the function so it would not be appropriate to just assign some huge value to g(), such as 2n. 

## Omega

## Theta
