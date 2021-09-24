# Complex number
## Reminders and historical approach 

1) Solving a 1st degree equation --> of the form `ax + b = 0` (with a ≠ 0)<br>
--> always only one solution: `x = -(b/a)`<br>
2) Solving a 2nd degree equation --> of the form `ax² + bx + c = 0`<br>
--> use `x = (-b ±√(b²-4ac))/(2a)`<br>
3) Solving the 3rd degree?<br>
--> always at least one solution, and at most 3.<br>
----> PoC why we've always at least one solution<br>
			`f(x) = x³ + x² + x + 1`<br>
			`lim(x->-∞) => f(x) = -∞` and `lim(x->+∞) => f(x) = +∞` <br>
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
2. In this equation, a and b are the unknowns. Bombelli then imagines imposing between a and b, a link that implies the writing, by posing `3ab + 15 = 0 or b = -5/a`<br>
Thus he kills two birds with one stone: he has only the unknown a left, and the equation is simplified:
```
a³ - (-5/a)² - 4 = 0
OR
a⁶ - 4a³ + 125 = 0
```
3. This equation is a biquadratic equation.<br>
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
Goal: to introduce a set larger than ℝ, in which all elements, even negative ones, admit a root of even index and to exploit these elements as tools for algebra, trigonometry, geometry, physics....: the set of **complex numbers**<br>
### New law
To "make" a complex number, use 2 real numbers --> use ℝ²

* Law already known about ℝ²:<br>
-- Internal law + : `ℝ² + ℝ² -> ℝ² : ((a,b),(c,d)) ~> (a+c, b+d)`<br>
Properties => (ℝ², +) = commutative group<br>
-- External law * : `ℝ * ℝ² -> ℝ² : (r,(a,b)) ~> (ra,rb)`<br>
Properties => `(ℝ,ℝ²,+)` = vector space of dimension 2<br>

* New law on ℝ²: <br>
-- internal multiplication * : `ℝ² * ℝ² -> ℝ²`<br>
Properties => `(ℝ²{(0,0)}, -)` = commutative group

### Construction of ℂ

__Preliminary remark__
- `(r,o) * (a,b) = (ra,rb) = (a,b) * (r,o)` // `r` and `(r,o)` are 2 elements of very different sets but play a similar role.
- `r * (a,b) = (ra,rb) = (a,b) * r` -> "identify" them by an isomorphism

* Let `P = {(a, 0) | a ∈ ℝ} ⊂ ℝ²` (represented in the Cartesian plane by the X axis)

* `f : P -> ℝ : (a,0)` ~> a is a **bijection** that respects the + law because `f((a,0)+(b,0)) = f((a,0)) + f((b,0))` and the * law because `f((a,0) * (b,0)) = f((a,0)) * f((b,0))` 

This is an isomorphism => same properties in the 2 fields `(ℝ, +, *)` and `(P, +, *)`<br>
=> each pair of type (a,0) will be noted **a** *note that (a,0)≠a*<br>

* What about the other pairs?
`(a,b) = (a,0) + (0, b) = (a, 0) + (b, 0) * (0, 1)` <br>
so i = new notation for (0,1), and (a,b) will be denoted `a + bi`
**N.B.** `(0,1) * (0,1) = (-1,0)`, which is noted **i² = -1**.
* i is called the **imaginary unit** (it is a square root of -1)
* A complex number = an element of ℝ² which has changed notation.
* The set of these numbers is noted ℂ

## Operations and calculation rules - properties
* Law +:
		In ℝ²: `(a,b) + (c,d) = (a+c, b+d)`<br>
	==> In ℂ: `a + bi + c + di = a + c + (b + d) * i`<br>

* Law \*:
		In ℝ²: `(a,b) * (c,d) = (ac - bd, ad + bc)`<br>
	==> In ℂ: `(a + bi) * (c + di) = ac - bd + (ad + bc) * i`<br>

* `(ℂ,+,*)` = fields because `(ℝ²,+,*)` is one.

* ℝ⊂ℂ because ℝ identified with P which is ⊂ℝ²

* Vocabulary: ∀Z ∈ ℂ, Z is uniquely written `a + bi`.<br>
	The real a is called the **real part** of z -> a = R(z)<br>
	The real b is called the **imaginary part** of z -> b = I(z)<br>

	if a = 0 and b ≠ 0, z = bi is **pure imaginary**<br>
	if a ≠ 0 and b = 0, z = a is real<br>

* 2 complex numbers are **equal** <=> they have the same real part and the same imaginary part i.e. `a + bi = c + di <=> a = c and b = d`

* 2 complex numbers are **conjugate** <=> they have the same real part and opposite imaginary parts:
	-> if `z = a + bi`, its conjugate = `a - bi`

* ∀Z ∈ ℂ: zˉz ∈ ℝ *(note that ˉz = z conjugate)* 
