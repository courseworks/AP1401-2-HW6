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

    $$ \int_{-1}^1 f(x) dx \approx \sum_{i=1}^n \omega_if(x_i) $$

    Such that $x_i$ is zeros of Legendre polynomials.
    By using the zeros of the Legendre polynomials, $\omega_i$ coefficients can be calculated by

    $$ \omega_i = \frac{2}{(1-x_i^2)[P_n'(x_i)]^2} $$

    Formulas 2 and 3 can be used to calculate several legendary sentences and their derivatives.

