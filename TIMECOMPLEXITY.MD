# Time complexity of Algorithms

In mathematical analysis, asymptotic analysis, also known as asymptotics, is a method of describing limiting behavior.


## Time Complexity Table



## Big-O

Big-O notation is used to classify algorithms based on the based on the number of operations or comparisons they use, typically big-O is used to the define the upper bounds, 
or worst case running time of a function. In plain words, Big O notation describes the complexity of your code using algebraic terms.

When we calculate big O notation, we only care about the dominant terms, and we do not care about the coefficients. Since we want to analyze the growth with respect to the input 
size, the coefficients which only multiply the number rather than growing with the input size do not contain useful information. The dominant term is the term that grows the fastest, a good way to think about this is that when **x** gets really large, consider the following: x² + 25x + 2000, when x is a million or a billion, then the values other than x² are insignificant.

For large values of x: x², 3x² + 25, 4x² + 7x + 75 which are all similar we will treat them all as the same order O(x²).

**Big O**: f(n) is O(g(n)) if for some constants c and N₀, f(n) ≤ c * g(n) for all N > N₀

***What this means is that f(n) grows no faster that g(n).***

g(n) = n²
c = 1
N₀ = 0
n = 1000

Using the above values N² will always be greater than (N²/2) - (N/2)

n² = 1, 000, 000
(N²/2) - (N/2) = 499, 500

When we talk about Big O, we want to know the tight bound of the function so it would not be appropriate to just assign some huge value to g(), such as 2ⁿ.

How can we show that: 3x² + 25 is O(x²)?

**Manually**

x = 5

3x² + 25 = 3(5²) + 25 = 25 * 3 + 25 = 100

Can we prove that: 

C(5²) ≥ 100 and as such c * 25 ≥ 100

So we can easily see that 4 fits this because: 4 * 25 = 100

So using this method we have found values for **k** and **C**: k = 5, C = 4

Up to this point we have shown that f(x) is *equal* to Cg(x) when k = x and now we need to prove that for all values of x > k this holds true.

x = 6
k = 5
C = 4

3(6²) + 25 = 133

4(6²) = 144

**Bumping everything up to the greatest power**

3x² + 25 ≤ 3x² + 25x²

3x² + 25x² = 28x²

3x² + 25x² ≥ 3x² + 25 when x > 1

It is important to remember that x must be greater than one for this to be true, because 0.5 * 0.5 = 0.25!

However as long as x > 1 we now have values for C and k.

C = 28
k = 1

We only need to find ***ANY*** C and k value that work.

## Omega

## Theta
