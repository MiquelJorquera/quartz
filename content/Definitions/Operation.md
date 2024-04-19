---
tags:  Maths/Logic/Set_theory
---
An $n$-ary *operation* is a [[Function#^Function|function]] $f:(X_1\times...\times X_n)\to Y.$ ^Operation

A *binary operation* is a [[Function#^Function|function]] $f:X_1\times X_2\to Y.$
It is very common to also demand [[#^Closed|closure]]. ^Operation2

An [[#^Operation|operation]] $f$ is *closed*, or *internal*, if $f:(X\times X\times...\times X)\to X.$ Shorthand for this is "Operation $f$ in $X$". ^Closed

A [[#^Operation2|binary operation]] $·:X\times X\to Z$ is *commutative* if $x·y = y·x.$ ^Commutativity

A [[#^Closed|closed]] [[#^Operation2|binary operation]] $·$ is *associative* if $(x·y)·z = x·(y·z).$ ^Associativity

The (left) *identity element* of a set $X$ with respect to a [[#^Closed|closed]] [[#^Operation2|binary operation]] in $X$ is an element $I\in X$ such that $I·x=x$ for all $x\in X.$ ^Identity

The (left) *inverse* of an element $x\in X$ of a set $X$ with respect to a [[#^Closed|closed]] [[#^Operation2|binary operation]] in $X$ is an element $x^{-1}\in X$ such that $x^{-1}·x=I,$ where $I$ is the [[#^Identity|identity element]] of $X.$ ^Inverse

Given two [[#^Closed|closed]] [[#^Operation2|binary operations]] $(*,+)$ on a set $X,$ the operation $*$ is *(left-) distributive over $+$* if $x*(y+z)=(x*y)+(x*z).$ ^Distributive

The *Jacobi identity* for two [[#^Operation2|binary operations]] $+$ and $\times,$ is$$x\times (y\times z)\ +\ y\times (z\times x)\ +\ z\times (x\times y)\ =\ 0$$ ^Jacobi