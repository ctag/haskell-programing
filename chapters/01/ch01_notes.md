### Chapter 1 Notes

#### Basics

Lambda calculus has three basic components (lambda terms):

* expressions
	* Superset of the others. Can be a variable or abstraction.
* variables
	* An input waiting for a value.
* abstractions
	* A function. Has a head (lambda) and a body. Is applied to an argument (input value).

Abstractions consist of a head and body. The head is a λ (lambda) followed by a variable name. The body of the function is another expression. 

	A simple function (identity function): λ x . x
	The head of the lambda: (λ x .)
	The body: (x)

Alpha equivalence:

* λx.x
* λd.d
* λz.z

Are all the same.

#### Beta Reduction

Apply the above identity function to 2:

	(λx.x) 	2
			2

Beta reduction is the process of applying a lambda term to an argument, replacing the bound variables with the value of the argument, and eliminating the head. Eliminating the head indicates the function has been applied.

Applying the identity function to another lambda abstraction:

	(λx.x) 	(λy.y)
	[x := 	(λy.y)]
			 λy.y

Again:

	(λx.x) 	(λy.y) z
	((λx.x)	(λy.y)) z
	[x := 	(λy.y)]
	(λy.y) 	z
	[y := 	z]
			z

#### Free Variables

	(λx.xy)

In the above: x is a bound variable because it is named in the head of the function, and y is a free variable because it is not. When the function is applied to an argument, nothing can be done with y, it remains un reduced.

#### Multiple Arguments

Each lamda can only bind one parameter, and can only accept one argument. When you apply it once and eliminate the leftmost head, the next one is applied, this formulation is called *currying*.

	λxy.xy
	λx.(λy.xy)










