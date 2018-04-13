---
title: Intro to Higher Math
heading: Can You Take Me Higher
subheading: What you need to know to start tackling math beyond calculus
author: Bradley Post
banner-pic: george.png
categories: math
layout: post
---
So, you decided that there is some math you don't know, that you should know. You looked it up and it's just a mess of weird symbols and words like group and graph, and you know what those words mean normally, but it seems like these mathematicians have a whole different idea about what they mean. If I'm describing you, then you've come to the right place. This article is an attempt to explain the basics of mathematical notation and convention, so that you are able to look at a proof, and at the very least know what most of the symbols mean. There are three main topics I'll cover:
* __Sets__
* __Quantifiers__
and
* __Commonly__ __used__ __operations__ __and__ __functions__

## Sets
If you haven't heard of a set before, then I'm surprised you ended up on a group theory tutorial. In any case, I'm going to explain sets and their notation in the interest of being comprehensive. A *set* is a collection of *elements*. Elements in a set have no structure whatsoever.They have no order. There is only one rule about the elements in a set, and that is that there cannot be any repeats. Every element in the set appears only once. There's a handful of other rules about sets, but they won't come up in what we're doing.

##### Unnecessary but interesting background information
(You can skip this paragraph)
Sets and set theory are the foundation of all mathematics. The way that we formally define them (generally this is done using [ZFC](https://en.wikipedia.org/wiki/Zermelo%E2%80%93Fraenkel_set_theory), but other ways of defining sets exist), likely has impact on what we can and cannot prove using mathematics ([G&ouml;del's Incompleteness Theorems](https://en.wikipedia.org/wiki/G%C3%B6del%27s_incompleteness_theorems)). There was a general conception of sets among mathematicians since the Greeks, but the first bonafide set theorist is generally considered to be Georg Cantor (1845-1918). He has some of the most interesting, important, and accessible proofs in all of mathematics, most of which dealt with infinite sets (ex: [Cantor's Diagonal Argument](https://en.wikipedia.org/wiki/Cantor%27s_diagonal_argument)). At the turn of the 20th century, the mathematician/logician Bertrand Russell (1872-1970) found a problem with the way sets were defined ([Russell's Paradox](https://en.wikipedia.org/wiki/Russell%27s_paradox)) and basically broke math on the whole. That is the reason ZFC was developed. Overall, sets have an interesting mathematical history, and it's certainly worth looking into if you're interested.

##### Back to the action
Now that you have an idea of what sets are, let's talk about how we write them down. The elements of a set are written inside a set of curly braces, like this:
 A $$\{1,2,3\}$$
This is the set containing the numbers 1, 2, and 3. But let's say we want to give a bigger set, where it would be inconvienent to write down all the numbers. Then we can write:
 B $$\{1, 2, 3, ... , 57\}$$
Using the ..., we basically are saying that the pattern at the beginning is repeated until you get to the number at the end. We can also indicate that the pattern carry's on *ad-infinitum*:
 C $$\{1, 2, 3, ... \}$$
This notation is fairly intuitive, but it can become tedious to write and confusing to use. We'll talk about more useful notation soon.

Generally, we classify sets in two major groups: *finite sets* and *infinite sets*. The names are pretty self-explanatory. Finite sets have a finite set of elements, and infinite sets have an infinite set of elements. A and B above are finite sets. C is an infinite set. Now, we'll talk about a couple of our favorite infinite sets.

#### Common Sets

The first set I'd like to tell you about is the empty set, or the null set. This is a set with no elements. Every set with no elements is the same. We can write it like this $$\{\}$$, just a set of brackets without any elements, but more often it is written like this $$\emptyset$$. This is not to be confused with something like $$\{\emptyset\}$$, as this is not the empty set, but a set containing the empty set. As stupid as it sounds, these are two different things.

Now, we'll talk about the natural numbers, also called the counting numbers. They begin at one and continue by counting up by one infinitely. We can write this as:
$$\{1, 2, 3, ...\}$$
Or, if you want to save time and do what every reasonable person does, you use the symbol $$\mathbb{N}$$, which stands for the set of all natural numbers. When you see $$\mathbb{N}$$, you can read it as "the set of all natural numbers". We also have the integers, which most people are familiar with. These include all the whole numbers and zero. We can define them like this:
$$\{...-2, -1, 0, 1, 2, ...\}$$
But, they have their own symbol, too. It is this fancy z, $$\mathbb{Z}$$. You may have also heard of the rational numbers, real numbers, and the complex numbers. Those use the symbols $$\mathbb{Q}$$, $$\mathbb{R}$$, and $$\mathbb{C}$$,  respectively.The rationals are all numbers that can be written as fractions. The reals are just, like, all the numbers or whatever. You'll get a clearer explanation when we define them in a few paragraphs. The complex numbers include imaginary numbers, or numbers that use the square root of -1 (i), real numbers, and combinations of real and imaginary numbers. I now encourage you to attempt to define these three sets with set notation. Don't scroll down and look at the answer, actually try.I'm in no hurry. Take your time.

#### Set Builder Notation
So, if you actually found a way to define the rationals, reals,  or complex numbers using only the notation I gave you above, then please send it to me (my email is bpost.brad@gmail.com). I'm geniunely interested. But, it is much easier to do if we give ourselves some more expressive notation. We call it set builder notation, and it allows us to build sets. It also draws upon some other mathematical notation, namely the symbols for qualifiers, so you may refer to that if you don't already know it.

So, say we want to define a set of all the even numbers greater than $$0$$. Well, we could do it like this:
$$\{2, 4, 6, ...\}$$
But, maybe we want to be more specific. Maybe, we want people to be sure what we are talking about, instead of just assuming that we mean even numbers greater than 1. Here's how we do it:
$$\{x\;| x = 2n \,\,\,where\,\,\,  n \in \mathbb{N}\}$$
This gives us the set of all even numbers, but this may not be immediately obvious. Really, what ends up happening is we are constructing a mathematical sentence. The way that it starts is by saying "The set of all x's...". Whenever there are curly brackets, then we are constructing a set, and the first variable generally tells  us what we are calling our elements. Then we move on to the $$|$$. This translates to "such that". Basically, it's giving some condition the x's have to follow. We can also write this as ":". "|" and ":" are used interchangeably. I'll be using "|" most of the time, but there are times where ":" makes things more readable. In any case, the x's have to follow the condition that $$x = 2n$$. Here, we're told that all of the x's (elements) of our set must be equal to double some number $$n$$, where $$n$$ is included in the set $$\mathbb{N}$$. The symbol $$\in$$ is used to indicate that an element is a member of a set. So, $$n \in \mathbb{N}$$, indicates $$n$$ must be a natural number. When we read this through, we get a sentence that says "The set of all x's such that x = 2n where n is a natural number." This is an equivalent set to all even numbers greater than zero. Every element in the set is given by multiplying a number equal to or greater than 1, and that gives us every even number. I encourage you to try to write the set of all odd numbers using set builder notation before we move on. It's fairly similar.

Did you do it? Cool. I'll just give you a few more examples of some sets expressed in set builder notation:

The set of all integers less than 0:
$$\{x \in \mathbb{Z} \;|\; x < 0\}$$
Note: In this instance, we have specified that x is an integer before the $$|$$. This is because x's type was not implied by our restrictions.


The set of all real numbers not equal to pi:
$$\{ x \in \mathbb{R} \; | \; x \neq \pi\}$$

The set of all square numbers:
$$\{x\;|\; x = n^2 \,\,\,where\,\,\, n \in \mathbb{Z}\}$$
Note: This one is interesting because squaring all the integers would give you 2 of every square number (positives and negatives both square to a positive), but since sets don't repeat themselves those numbers are just dropped. You are allowed to have definitions that repeat values, if that makes sense. They just won't be repeated in the set.

Now I'll reccommend that you try to define some sets with set builder notation. Here are some that you can try:
1. The set of all integers which are multiples of 3
2. The set of all numbers greater than 52, but less than 1,270,543
3. The set of all cubed numbers
4. The set of all numbers one less than a power of 2

#### Defining more number systems

Now that you have a feel for set builder notation, we can get to something a little more interesting, creating definitions for a more complicated number system. We'll start with defining the set of all rational numbers. The rationals are really just numbers made from dividing integers by other integers. Knowing that, it's not that hard. It isn't a bad idea to try and do this on your own. There are multiple ways to define the set, but this is the way I like to do it:
$$\{x \;|\; x = \frac{y}{z} \,\,\, where \,\,\, y, z \in \mathbb{Z}\}$$
So, if we decode this to a verbal form, then we have "The set of all numbers $$x$$ such that $$x$$ is equal to $$\frac{y}{z}$$ where y and z are integers."
We can do something similar for the real numbers, but it's actually a lot more involved. A definition of the reals that achieves sufficient mathematical rigor only came about fairly recently (around the same time math got broken by Russel). I'll write about how we do that somewhere else. But, if we take the reals for granted, it isn't very hard to define the complex numbers. The first thing we have to do is let $$\sqrt{-1} = i$$. Since the complex numbers are all a sum of real and imaginary parts, then we have:
$$\{c \; | \; c = a + bi \,\,\, where \,\,\, a, b \in \mathbb{R}\}$$
At this point, I think you can probably start figuring what these set builder definitions mean on your own.

#### Subsets
You may be asking yourself, "Some of these sets are pretty big, I wish I could just have a little part of them." You're in luck, we don't have make all of our sets based on giant infinite sets. Instead, we have these useful objects we call *subsets*. An observant reader would be able to think of some subsets based on what we have already. But, how do we write that down? Like this:
$$\mathbb{N} \subset \mathbb{Z}$$
This says that the natural numbers are a subset of the integers. This is intuitively obvious, as every natural number is included in the integers. Another symbol that comes up a lot is $$\subseteq$$. This indicates that a set is a subset of another set, or the two sets are equivalent. Mathematicians like to use this one a lot, because sometimes they aren't sure whether a set has some of the elements in another set, or all of them. Of course, it's perfectly legal to write:
$$\mathbb{N} \subseteq \mathbb{Z}$$
But, a more illustrative example occurs if I define some new sets. Let A be a set where we know all it's elements are integers. Let a set B be given by $$B = \{x \in A | x = 2n \,\,\, where \,\,\, n \in \mathbb{Z}\}$$. Then we know $$B \subseteq A$$, but we can't say for sure that $$B \subset A$$. Can you see why? Right. Because A may or may not be made up entirely of even integers. When we talk about these symbols, we would say "B is a subset of A" either way. But, in the first case, we can "$$\mathbb{N}$$ is a *proper* subset of $$\mathbb{Z}$$. A fun thing that every math teacher writes on the board whenever they teach subsets is this statement:
$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{R} \subset \mathbb{C}$$


There's a lot more to know about sets, but this page isn't about teaching everything about set theory. I'll give you more information about it somewhere else.

## Quantifiers
Quantifiers were invented by mathematicians so they wouldn't have to write a bunch of words down when they were explaining things. At first, most people find them to be a little strange, but after you get used to them they make life a lot easier. There are two important ones: $$\exists$$ and $$\forall$$. $$\exists$$ means "there exists", and we call it the *Existential Quantifier*. $$\forall$$ means "for all" or "for every", and we call it the *Universal Quantifier*. Basically, we can use these to make more interesting mathematical statements. For example we can write things like $$\forall x \in \mathbb{Q} \,\,\, where \,\,\, x \neq 0 \;\; then \exists y \in \mathbb{Q} \,\,\,such\;that\,\,\, \frac{x}{y} = 1$$. Basically, we've got a statement that says every rational number other than $$0$$ can be divided by another rational number so that you get $$1$$. We can put a slash through $$\exists$$ too, so we have $$\not \exists$$ ("there does not exist"). $$\not \forall$$ doesn't really come up, because it pretty much means "The opposite pf the following statement is true for all...", and that's kind of clunky to work with. 

Often times, the english words in the statements will get left out. For the statement above, we could simply write:
$$\forall x \in \mathbb{Q},\; x \neq 0, \; \exists y \in \mathbb{Q}, \frac{x}{y} = 1$$
This has an identical meaning, but is a little harder to read right off the bat. Instead of commas, you may also see parentheses:
$$(\forall x \in \mathbb{Q}) (x \neq 0) (\exists y \in \mathbb{Q}) \frac{x}{y} = 1$$
There's a whole bunch of different ways to write this statement. Personally, I like to just write out the extra words in the interest of readability, so that's what you'll be seeing from me down the line.

Here are some more examples. Try to write the mathematical statements in plain english. decide whether the statement is true or false:
Let A be the set of all odd integers. $$\forall x \in A,\; \exists n \in \mathbb{Z}\,\,\,such\:that\,\,\,x = 2n-1$$.
$$\forall x \in \mathbb{R}, \; \exists y \in \mathbb{R} \,\,\, such\;that\,\,\, x=y^2$$
$$\exists x \in mathbb{R}, \,\,\,such\;that\,\,\, \forall y \in mathbb{R}, \; x = y^2$$
$$\forall x,y \in \mathbb{R},\; \exists z \in \mathbb{R} \,\,\,such\;that\,\,\, x^2 + y^2 = z$$
$$\exists x, y, z \in \mathbb{Z}\,\,\, such\;that\,\,\, x^2+y^2=z^2$$
$$\forall x,y \in \mathbb{z},\; \exists z \in \mathbb{z} \,\,\,such\;that\,\,\, x^2 + y^2 = z^2$$

If you understand the statements above, then you at least have a working understanding of the Existential and Universal Quantifier.

## Commonly Used Operations, Functions, and Terms

There are a lot of symbols, operations and functions used in math that someone without formal math knowledge might not recognize. You've probably heard of these things, and maybe seen them written in a different way, but this is how they are often addressed in proofs and mathematical texts.

#### Modulo

Modulo basically just gives the remainder of a division problem. If you've done some programming, then you know about it. In math, we have some specific symbology. Let's say we want to write that the remainder of 7 divided by 3 is equal to 1. It would look something like this:
$$1 \equiv 7 (\pmod 3)$$ or $$1 \equiv 7 \mod 3$$
Sometimes people use the parentheses, sometimes they don't. It's a matter of preference. The triple line equal sign indicates congruence, as opposed to equivalence. This is a convention of modular arithemetic in math. We could also write something like:
$$6 \mod 5 \equiv 7 \mod 3$$
$$\frac{6}{5}$$ has a remainder of 1, and $$\frac{7}{3}$$ has a remainder of 1, so we can say they're congruent. There's a bit more to modular arithmetic, but I'm not going to cover that here.

#### Divides: "&#124;"

So, we talked about "&#124;" when working with set builder notation above. But, the it also gets use as a symbol meaning "divisible by". So, we can write something like $$ 3$$ &#124; $$ 6$$. This means 3 divides 6 evenly (with no remainder). We can also write $$3 \not | 7$$ . This generally is only used in reference to integers, but it also comes up in reference to polynomials and some other mathematical objects. One more example: $$ x, y \in \mathbb{Z} \,\,\, where \,\,\, x=2y, \; then\,\,\, 2 \vert x$$

#### Ceiling "$$\lceil\,\,\rceil$$" and Floor "$$\lfloor\,\,\rfloor$$"

The ceiling function gives the nearest integer greater than the input number. For example, $$\lceil 2.01\rceil=3$$. The floor function gives the nearest integer less than the input number. So, $$\lfloor2.99\rfloor=2$$.

#### Function Notation

You're probably used to seeing a function written as $$f(x) = x$$. But, to rigorously define a function, we also have to give the sets corresponding to its domain and codomain. So, we have a little more symbology. If we have a function $$f$$ we want to map from a set $$A$$ to a set $$B$$ (when I say map, I mean that we give each element in the set $$A$$ and value in the codomain $$B$$), we would write $$f: A \rightarrow B$$. Next, we would define our function. So, in total it looks something like this: $$f:A\rightarrow B, f(x) = x$$. If, for example, we wanted to map the real numbers to the real numbers, we would write: $$f:\mathbb{R}\rightarrow\mathbb{R}, f(x) = x$$ (giving us the standard linear function we all know and love).  

#### Function Composition $$(f\circg)(x)

The little circle is the symbol for function composition. It indicates that you take the output of the function to the right and pass it as the input of the function to the left. So, the input is from the domain of rightmost function, and the output is from the codomain of the leftmost function. Say we have two functions, one that maps from the integers to the positive square roots of the integers, called $$g$$, and one that maps from the positive square roots of the integers back to the integers, called $$f$$. The first thing we would do is define a set of the positive square roots of all the integers. We'll call that set $$S$$, then $$S = \{x \in \mathbb{R} | x = \sqrt{y}\,\,\forally\in\mathbb{Z}\}$$. Now, we can write the following functions: $$f:S\rightarrow\mathbb{Z}, f(x)=x^2$$ and $$g:mathbb{Z}\rightarrow S, g(x)=\sqrt{x}$$. Using these we can define the function $$f\circ g:\mathbb{Z}\rightarrow\mathbb{Z}, (f \circ g)(x) = (\sqrt{x})^2 = x$$. Notice that we applied the rightmost function first, and the leftmost function second. We can do this for longer strings of functions. For example: $$g\circ f \circ g:\mathbb{Z} \rightarrow S, (g\circ f \circ g)(x) = \sqrt{(\sqrt{x})^2}$$, which you can probably tell is equivalent to $$g$$. Notice how I have carefully defined the domains and codomains so that every element of the domain is used as an input, and the element of the codomain is used as an output. This is the standard for a proper function definition. Also, the unless given explicity, the square root function returns only positive values.



