---
layout: page
title: Path Independence
order: 1
permalink: /path_independence/
---

Consider the graph representing a category such that every path between a common source and sink is equal. 
Such <em>path independent graphs</em> arise frequently in practice- from the implicit type conversion graph for a program in languages like scala, to the category of units of measure where morphisms are conversions between the units.
It is often useful to be able to check that a graph indeed stays path independent over the course of its construction. I am working on efficient ways to perform such verification.

As a case study to evaluate the idea, we are implementing the ideas in the compiler of Gator, a domain specific programming language for geometry types. Our algorithm is used to ensure that user defined transformations between spaces stay consistent, and the compiler, deterministic as it makes automatic conversion choices.