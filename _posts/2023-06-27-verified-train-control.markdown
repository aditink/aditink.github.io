---
layout: post
title:  "A Verified Train Protection System"
date:   2023-06-27 12:07:06 -0400
categories: literature
---

Train protection systems safeguard railroad operation by keeping motion within a safe envelope, deciding when to slow trains down to avoid collisions with other trains on the track, stay inside movement authorities (the region of the track that a signalling system allows a train to be in), and navigate slopes, curves, and tunnels safely.
Given the frequency and deadliness of train safety incidents around the world, train protection software has a huge potential for positive impact.
But how do we make sure that the train protection software _itself_ is correct?
The standard in industry currently is to run extensive, expensive tests and simulations.
While this testing goes a long way in catching bugs, it is still not completely reliable.
Reality restricts engineers to performing a finite number of tests, checking only a small fraction of the infinitely many situations that a train protection system might face.
Train motion is complicated and involves many parameters, and train infrastructure is complicated with many moving parts and communicating subsystems.
Testing is simply too limited a technology to check every scenario and catch every bug.

## Formal Verification

This is where formal verification enters the picture.
The idea is to model the train control software as well as train subsystems and dynamics mathematically, in a suitable logic.
Within this logic, following mathematical rules, we write a _proof of safety_.
The nice thing about mathematical proofs is that when they succeed, they provide a complete guarantee, checking safety in every modeled scenario.
Thus, a single formal proof corresponds to infinitely many simulations.
To get a really rough idea of how this might work, think back to middle school math.
Suppose that you know for a fact that `x<y+1`.
You now want to check if `x+y<1`.
On the one hand, you could write a simulation: run a program that assigning different values to `x` and `y`, and check if things work out. But there are an infinite number of combinations of `x` and `y`, and you will never be able to check all the possibilities.
But instead, mathematical rules allow us to perform algebraic transformations that are always correct: if `x<y+1`, then `x-y<y+1-y`, which simplifies to `x-y<1`.
By using mathematical rules, we were able to derive the conclusion we were interested in checking with 100% certainty.
Train controllers are certainly a lot more complicated, but the same idea applies: use mathematical transformations to derive conclusions about the controller with certainty.
Further, to preclude the possibility of human error in the math, a computer checks the proof to certify that it works out.

## Why Formal Verification?

Being certain about correctness is very valuable.
Not only does it save lives and provide peace of mind, but also, precision in reasoning can permit more aggressive, efficient train operation.
No longer would engineers have to leave conservative margins for errors that they can not precisely reason about.
Trains scheduled closer together can mean increased throughput.
Likewise, as trains driven by artificial intelligence become a possibility, it is more important than ever to secure efficient but poorly understood machine learning-based decisions within trustworthy, highly reliable train protection software.
Knowing that the train protection software handles every edge case correctly becomes essential.
Formal methods-based verification can also make it easier to handle updated system requirements than simulations.
Instead of rerunning an entire test suite, only relevant modification in the proof would be required.

## A Proof of Concept Verified Train Protection System

As a proof of concept, we created a verified train protection system.
We proved the train protection safe against the train kinematics model from [1] (the FRA paper that develops a PTC braking algorithm for freight trains).
We sought to design a mathematically sophisticated train protection system that was provably safe while still being as efficient as possible.
The technical challenges are summarized in [our paper at EMSOFT 2022](assets/train-control-emsoft-preprint.pdf), and also in [this video](https://www.youtube.com/watch?v=TKRSZA_61cM) of the corresponding talk.
Running some experiments to understand the behavior of our system, relative to the PTC algorithm specified in [1], we found scenarios where the verified protection system a 4X improvement in reducing the undershoot during braking enforcement.
The train protection system that we created was symbolic, meaning that by substituting in concrete values for the various parameters via the appropriate methods [2], we can easily obtain concrete verified controller tailored to specific railroads and trains.
I am interested in closing the gaps between the current state of the art in verification and what industry would find useful in practice so that train control can benefit from formal verification.

## References

[1] J. Brosseau, B. M. Ede, S. Pate, R. Wiley, and J. Drapa, “Development of an operationally efficient PTC braking enforcement algorithm for freight trains,” Tech. Rep. DOT/FRA/ORD-13/34, 2013.

[2] A. Platzer, “A complete uniform substitution calculus for differential dynamic logic,” J. Autom. Reas., vol. 59, no. 2, pp. 219–265, 2017.