# Complex number
## Reminders and historical approach 

1) Solving a 1st degree equation --> of the form `ax + b = 0` (with a ≠ 0)<br>
--> always only one solution: `x = -(a/b)`<br>
2) Solving a 2nd degree equation --> of the form `ax² + bx + c = 0`<br>
--> use `x = (-b ±√(b²-4ac))/(2a)`<br>
3) Solving the 3rd degree?<br>
--> always at least one solution, and at most 3.<br>
----> PoC why we've always at least one solution<br>
			`f(x) = x³ + x² + x + 1`<br>
			`lim(x->-∞) => f(x) = +∞` and `lim(x->+∞) => f(x) = -∞` <br>
4) To find the __integral roots__: Horner's method (1786 - 1837)<br>
5) To approximate non-integer __roots__: graphical, dichotomous methods....<br>
--> Dichotomy<br>
----> Bolzano's theorem<br>
----> On the interval AB we use Bolzano's theorem; we divide the interval AB until equals a change of sign.<br>
<br>

Let the equation `x³ - 15x - 4 = 0` be used.<br>
-> with Horner: 4 is found as a solution<br>
In the 16th century, __Bombelli__ solves the following equation in the following way:<br>
1. He writes `x` in the form `a - b` -> the equation becomes:
```
(a-b)³ - 15(a-b)-4=0
a³ - 3a²b + 3ab² - b³ - 15(a-b) - 4 = 0
a³ - 3ab(a-b) - b³ - 15(a-b) - 4 = 0
a³ - (a-b)(3ab+15) - b³ - 4 = 0
```
2. In this equation, a and b are the unknowns. Bombelli then imagines imposing between a and b u, a link that implies the writing, by posing `3ab + 15 = 0 or b = -5/a`<br>
Thus he kills two birds with one stone: he has only the unknown a left, and the equation is simplified:
```
a³ - (-5/a)² - 4 = 0
OR
a⁶ - 4a³ + 125 = 0
```
3. This equation is a bicarbonate equation.<br>
By positing `a³=t`, it becomes: `t² - 4t + 125 = 0`. But `ρ = -484 = 4 * 121`.<br>
To continue his reasoning, Bombelli assumes the existence of an **imaginary number**<br>
`√(-1)`, denoted later **i**, of square equal to -1.<br>

--> `ρ = 4 * 121 * i²` ---> `t = (4 ±2*11*i)/2 = 2±11*i`<br>
4. From the 1st value of t, he finds `a = 2 + i` because `a³ = (2+i)³` which is equivalent to `2³ + 3*2²*i + 3*2*i² + i³ = 8 + 12*i - 6 - i = 2 + 11*i` and thus `x = a - b = (2 + i) - (-2 + i) = 4`!!!<br>
For Bombelli, `i² = -1` was a useful fiction: using this imaginary i (which disappears during the calculation), the real solution was found.<br>
<br>
* By imitating Bombelli, we can find solutions to the equation `x² + 1 = 0`.
* In fact, it is like:
```
x + 3 = 0; has no solution for the one who only knows the naturals (ℕ)
2x + 5 = 0; has no solution for the one who knows only integers (ℤ)
x² - 2 = 0 ; has no solution for the one who knows only the rationals (ℚ)
x² + 1 = 0 ; has no solution for the one who knows only the reals (ℝ)
```
**ℕ ⊂ ℤ ⊂ ℚ ⊂ ℝ**


## Towards a new set
Goal: to introduce a set larger than ℝ, in which all elements, even negative ones, admit a root of even index and to exploit these elements as tools for algebra, trigonometry, geometry, physics....: the set of **complex numbers**
