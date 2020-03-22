---
layout: page
title: Path Independence
order: 1
permalink: /path_independence/
---

Consider the category theory construction where every path between a common source and sink is equal. 
Such <em>path independent graphs</em> arise frequently in practice- from the implicit type conversion graph in programming languages like scala, to the category of units of measure where morphisms are conversions between the units.
It is often useful to be able to verify that a category is indeed stays path independent over the course of construction. I am working on efficient ways to perform such a check.

As a case study to evaluate the idea, we are implementing the algorithm in the compiler of Gator, a domain specific programming language for geometry types, in order to ensure that user defined transformations between spaces stay consistent.  