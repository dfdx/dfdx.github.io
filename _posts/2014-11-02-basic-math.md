---
title: Basic Math
layout: default
---

# Basic Math

Many posts in this blog will discuss mathematical and statistical techniques, so it's worth to define core concepts we will utilize. This post is about math basics, while next one will be about probability theory. 

Though mathematics is pretty diverse field of science, it's build on top of not that many basic ideas. Here I describe 4 of them: sets, tuples, vectors and functions. 

## Sets

Set is simply collection of objects. Example sets are: set of metro stations in some city, set of colors of a traffic light, set of real numbers between 0 and 1, etc. Sets are normally written as an enumeration of its elements in curly braces (e.g. $\\{1, 2, 3\\}$ or $\\{r, y, g\\}$) and named with a bold upper-case letters (e.g. $\mathbf{C} = \\{r, y, g\\}$ or $\mathbf{R}$ to represent set of all real numbers). 

Two most important properties of sets are: 

 1. All elements in a set are <b>unique</b>. E.g. $\\{1, 2, 3, 2\\}$ is not really a set, because 2 occurs twice. 
 2. Sets are <b>unordered</b>. That is, $\\{1, 2, 3\\}=\\{3, 2, 1\\}=\\{2, 1, 3\\}$. 

There's also one universal empty set that contains no elements. 

## Tuples

Unlike set, tuple is an <b>ordered</b> collections of elements. If you came from software development, you should already be familiar with a concept of a tuple in databases (or even some programming languages like Python). In databases, tuple represents single row of data, e.g.: 


 |   sex    |   age  |  marital status  |   height  |  balance  |
 |----------|--------|---------------|-----------|-----------|
 |  female  |   26   |     single    |    168    |   2182    |
 {: .table .table-bordered}


In maths it is exactly the same thing (though maybe without column names): 

  $$(female, 26, single, 168, 2182)$$

As you should notice, order is crucial here: 26 year old woman of the average growth must be much prettier than an old lady of 168 years and only 26cm in height. Also note that it's allowed to have repeating elements in a tuple - it's ok to be 168cm in height and have 168 euros on credit card.  

Besides a role of data container, we will use tuples to describe other mathematical objects. For example, in algebra _ring_ is defined as a 3-tuple $(E, +, \times)$, where $E$ is some set, while $+$ and $\times$ are operations of addition and multiplication (obvious example of a ring is a set of relational numbers and mentioned operations on them).

One last thing about tuples. If elements $e_1, e_2, ..., e_n$ of a n-tuple belong to sets $S_1, S_2, ..., S_n$ respectively, then we say that the tuple itself belongs to a <b>Cartesian product</b> of these sets - $S_1 \times S_2 \times ... \times S_n$. Cartesian product of sets is easy to understand by example of card deck. If we have a set of card values $V = \\{6, 7, 8, 9, 10, J, Q, K, A\\}$ (9 items) and a set of suites $\\{C, D, H, S\\}$ (4 items), then Cartesian product of these sets is a set of all pairs $(Value, Suit)$ (9 * 4 = 36 items), i.e. the whole deck. 

## Vectors (and Matrices)

"<b>Vector</b>" is just another name for "tuple". That's it. End of the story. Well, not quite. Though technically term "vector" is used as a synonym for "tuple" in most fields, it normally has different notation and used in different contexts. The field that works with vectors most often is <i>linear algebra</i>, and standard notation for a vector there is a column of items in squared brackets: 

  $$v = \begin{bmatrix}
     2 \\\\ 4 \\\\ -5 \\\\ 1
  \end{bmatrix}$$

Note, that despite vertical orientation for vectors, for equivalent tuples we continue to use horizontal layout:

  $$v = \begin{bmatrix}
     2 \\\\ 4 \\\\ -5 \\\\ 1
  \end{bmatrix} = (2, 4, -5, 1)$$

But isn't vector that funny arrow from one point to another? 

<img src="http://hsto.org/files/0a7/2d7/142/0a72d714231e48628731fc8aedd8eb3c.gif"/>

Actually, it is. But in linear algebra we <i>bind the beginning of the vector to the origin</i>. The end of the vector in this is case is nothing more than a point in an n-dimensional space, which may be defined by an n-tuple:

<img src="http://oi43.tinypic.com/2wc45d1.jpg"/>

In this blog I will use words "tuple", "vector" and "point" interchangeably. 

But why do we need vectors? Because they are convenient. The analogy with geometry gives us intuition about how to model objects from real world. E.g. we know that point $(1, 2)$ is close to $(1, 3)$, but pretty far from $(0, -4)$. Same way we know that person $(female, 26, single, 168, 2182)$ is somewhat similar to $(female, 25, single, 172, 1900)$, but very different from $(male, 64, married, 185, 12800)$. We can calculate <i>distance</i> between two objects, or say that two properties of an object are independent from each other with a notion of <i>orthogonality</i>, or perform complex image transformations by means of simple formula on vectors. Linear algebra is the main workhorse for most other fields of maths, and vectors are in the very essence of linear algebra. 

Vectors describe real world objects, it's easy to understand. But what about matrices? Unlike vectors, tuple or sets, matrices are not inherent in mathematics, but instead are just a convenient way to represent sets of vectors. Originally they were used to easier solve systems of linear equations (see, for example, <a href="http://mathworld.wolfram.com/Matrix.html">Wolfram Mathworld</a>), and now are one of the most powerful tools of linear algebra. Matrices are commonly written as tables of items in square brackets: 

$$M = \begin{bmatrix} 3 & 15 & 10 \\\\ 8 & -1 & 5 \end{bmatrix}$$

Here $M$ is a $2 \times 3$ matrix (recall that first number is a count of rows, second - count of columns). It may be thought 
 of as 3 vertical vectors or 2 horizontal, or just as a table of numbers - no constraints here. Also note how similar are vector and matrix notations. In fact, it's quite common to think of vectors as 1-column matrices (though many software packages treat them differently). 

There are many useful operations over matrices. I'm not going to discuss them here, but if you plan to dive into linear algebra, recall transposing, scalar and matrix-matrix multiplication. 


## Functions

In maths function is somewhat different from what we are used to see in programming. In maths, <b>function</b> (or, equivalently, <b>map</b>) is a <i>relation</i> that assigns to every element from an input set some element from an output set. It may be easier to understand using following notation: 

$$f: X \rightarrow Y$$

which we read as "function $f$ maps elements from $X$ to elements from $Y$". In this sense mathematical functions are much closer to associative arrays in programming rather than pieces of code. 

Relation between $y \in Y$ and $x \in X$ may be given by formula: 

$$y = f(x) = x^2$$

by set of rules: 

 $$
  y = sign(x)=\begin{cases}
    1, & \text{if $x > 0$} \\\\
    0, & \text{if $x = 0$}\\\\
    -1, & \text{if $x < 0$}
  \end{cases}
$$

or simply stored (e.g. as pixels in image $I$): 

 $$y = I(i, j)$$


That's it. Four simple concepts (three if you count tuples and vectors as one). Not that many. But you will be surprised how powerful they are. 

