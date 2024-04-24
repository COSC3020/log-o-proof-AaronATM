[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

Proof:

Let $c$ be any positive integer, $a$, $b$ be any arbitrary constants, $n_0$ be any integer, $x(n)$ be a function such that $x(n) = \log_{a} n$, and $g(n)$ be a function such that $g(n) = \log_{b} n$.

By the change of base property of logarithms $x(n) = \frac{log(n)}{log(a)}$ and $g(n) = \frac{log(n)}{log(b)}.

This means that $\forall n \geq n_0$, $0 \leq x(n) \leq \frac{c}{log(a)}log(n)$ and $\forall n \geq n_0$, $0 \leq g(n) \leq \frac{c}{log(b)}log(n)$.

By the constant absorption property of big O notation, $x(n) \in O(log(n))$, and $g(n) \in O(log(n))$. 

Due to the fact that big O describes function growth rate, $O(\log_{a} n)$ is the same as $O(\log_{b} n)$ for any arbitrary constants a and b.

Thus, $O(\log_{2} n)$ is the same as $O(\log_{5} n)$.
