# Advanced Programming - HW6

<p  align="center"> <b> Homework 6 - Spring 2023 Semester   <br> Deadline:---------- </b>
</p>

Answer questions:

1. Functions in python are defined as follows:

    ```python
    def func(a, b, c, ..., *args, **keywords):
    ```

    Explain the last two arguments and their application with examples.

2. Consider the following codes:

    ```python
    A0 = dict(zip((’a’, ’b’, ’c’, ’d’, ’e’), (’1’, ’2’, ’3’, ’4’, ’5’)))
    A1 = range(10)
    A2 = [i for i in A1 if i in A0]
    A3 = sorted(A0[i] for i in A0)
    A4 = [[i, i*i] for i in A1]
    ```

    * Write the output of each line without running their.
    * Write the code to print all the variables of A0...A4 with one loop.

3. We want to estimate $\pi$.

    First, consider a square with side 1 and enclose a circle in it. In this order, first define a function `IsInCircle(x, y)` that determines whether a point is inside the circle or not. Then, by generating the number of random points that are inside the square, calculate the ratio of the number of points inside the circle to the total number of points. This ratio is equal to $\pi$. In this way, write the `find` function in such a way that determines how many random points should be at least in order to reach an error of one percent. (adding random points until we reach the desired error)

4. We want to calculate $\int_a^b f(x) dx$ with Gauss method. The working method is that we can approximate any integral between -1 and 1 by the following formula:

    $$\int_{-1}^1 f(x) dx \approx \sum_{i=1}^n \omega_if(x_i)$$

    Such that $x_i$ is zeros of Legendre polynomials.
    By using the zeros of the Legendre polynomials, $\omega_i$ coefficients can be calculated by

    $$\omega_i = \frac{2}{(1-x_i^2)[P_n'(x_i)]^2}$$

    Following formulas can be used to calculate Legendre polynomials and their derivatives.
    $$P_0(x)  = 1, P_1(x)  = x, nP_n(x)  = (2n-1)xP_{n-1}(x) - (n-1)P(n-2)(x)$$
    $$P_n'(x) = \frac{n}{x^2-1}(xP_n(x) - P_n-1(x))$$

    For find zeros of Legendre, use `newton-raphson` method. For initial guess use:
    $$x_0 = cos\left(\pi\frac{i-\dfrac{1}{4}}{n + \dfrac{1}{2}}\right)$$

    Hint:
    $$\int_a^bf(x)dx \approx \frac{b-a}{2}\sum_{i-1}^n\omega_if(\frac{b-a}{2}x+\frac{b+a}{2})$$

    - suppose $f(x) = \dfrac{x^3}{x+1}cos(x^2), \quad a = 0, \quad b = 1$
    - use recursive function to find Legendre polynomials.
    - This program is written with CPP programming language as Object Oriented and is attached. The input of this program is the number n, that is, the degree of Legendre's multi-sentence. You can also check your answer with this [link](http://www.wolframalpha.com/input/?i=int(((x%5E3)%2F(x%2B1))*cos(x%5E2),+0,+1)).
    - Write the program in a similar way using python programming language and measure the execution time. Make sure to write the program in OOP form, that is, using the class.
    - By `subprocess` library run cpp code in python and measure the execution time.
    - print the table that its rows are n and columns are execution time of cpp and python code.
    - plot this table with `matplotlib` and save it in `result.pdf`.(with code)

5. You are given an array of numbers. We call a number special if it is divisible by 6 and if its number is divisible by 6 at least in one of the positions that appear in the array. Note that the index of the first member of the array starts from 1.

    - input: array of numbers.
    - output: In the output line alone, special numbers are printed in ascending order so that there is a space between both numbers. Note that each special number appears exactly once in the output.
    - example:
      - input1: 
        ```python
        3 4 1 37 21 18 23 21 27 22 43 21
        ```
      - output1:
        ```python
        18
        ```
      - input2: 
        ```python
        1 2 3 4 5 6 7 8 9 10 11 12
        ```
      - output2:
        ```python
        6 12
        ```
        <br/>
<p  align="center"> <b>GOOD LUCK</b> </p>
