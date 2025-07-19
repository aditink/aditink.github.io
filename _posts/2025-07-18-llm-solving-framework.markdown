---
layout: post
title:  A Model to Predict LLM Effectiveness
date:   2025-07-18 12:00:00 -0400
categories: draft
---

_Aditi Kabra, [Margarida Ferreira](https://marghrid.github.io/), [Sagar Bharadwaj](https://sagar-bharadwaj-ks.github.io/)_

This blogpost presents a framework for predicting what problems LLMs are good at and what problems they would struggle with.
It divides problem solving into four techniques, some of which LLMs are better at than others.
LLM performance on a problem can then be predicted by the kind of operations that the solution requires.

The four techniques that we decompose problem-solving into are:
 1. *algorithmic computation*, which is executing a step-by-step procedure,
 2. *retrieval from memory*, which is recalling known facts,  
 3. *identifying decompositions*, which is breaking complex problems into simpler ones, and  
 4. *identifying abstractions*, which is recognizing shared structure across problems.

Sometimes, different combinations of techniques can solve the same problem.
For example, memorizing answers can compensate for slow or inaccurate algorithm execution.
On the other hand, some problems are hard to solve without the right technique.
For example, formalizing a novel idea described in natural language as a mathematical theorem requires the ability to *create abstractions*.
For each problem solving technique, the properties we desire in a problem solving approach (such as querying an LLM), are:
1. *accuracy*, that is, when an answer is provided, it is correct;
2. *efficiency*, where reaching the answer consumes minimal time and energy, and
3. *generality*, that is, ready applicability to most questions without special intervention.

How do LLMs, as problem solving approaches, shape up for each problem solving technique?

1. *Algorithmic computation*, for example, multiplying two numbers following the multiplication algorithm.
   Traditional computing (that is, symbolic AI) is very good at this.
   In comparison, humans and LLMs are inefficient and inaccurate.
   When multiplying two very large numbers, a traditional computer program will likely produce the correct answer faster than humans or LLMs that don't have access to calculators or traditional computing.
   On generality all three approaches perform well: symbolic AI is fairly general, able to execute any computable algorithm, while humans and LLMs can in principle simulate any algorithm.

2. *Retrieval from memory*, for example, recounting the name of a specific bone in the human body.
   Traditional computing accomplishes this well already, using the Internet, where humanity has collectively created a vast store of information.
   For most questions about the world, a Google search turns up more information than most humans can recall.
   LLMs are also very good at remembering information about the world, as they are trained on the internet, though perhaps a bit worse than traditional computing.
   LLMs suffer on generality because of information lost during the training process, which might lead them to forget information that is not well represented in the training data.
   They are generally less energy efficient, and they are less accurate due to hallucination.
   Humans are in comparison less general with less information memorized, and usually slower, especially when recalling older memories of more obscure facts.

3. *Identifying decompositions*, which is recognizing how to break down a problem into sub-problems, and stitching the pieces back together.
   For example, counting the number of bones in the human body that end with suffix “-oid” can be *divided into*  
   (1) recalling the names of all bones,  
   (2) filtering this list to keep only names ending in “-oid”, and  
   (3) counting them.
   Symbolic AI cannot do this at the level of generality required to solve most real-world problems out-of-the-box.
   In practice, divide-and-conquer procedures are hand-designed for specific domains and encoded as algorithms.
   LLMs begin to show the ability to break general problems down, especially in the more recent reasoning models.
   But for unseen problems, humans are currently more accurate.
   Indeed, problem decomposition is fundamental to how we operate, letting us solve our most complex problems by breaking them down into more manageable pieces, delegating some pieces to specialized experts, and yet other pieces to tools such as computer programs.

4. *Identifying abstractions*, that is, viewing objects as a coherent subset of their behaviors or properties, thus becoming able to recognize the abstract similarities (and differences) between them.
   This is what lets us convert word problems into mathematical equations and back.
   Symbolic AI again cannot do this at the level of generality that solves most real-world problems.
   LLMs begin to show the ability to reason with abstraction for real world objects and ideas.
   But currently, in our experience, well-trained humans are more accurate and creative.
   Understanding and working with abstractions is again a fundamental part of modern human existence.
   In everyday life, society is an abstraction that lets people interact with the 8 billion other people in the world without getting overwhelmed by reasoning about every individual's role.
   At the leading edge of human problem-solving ability, much work can be seen as humans finding the right abstractions to predict or explain the behavior of the world, such as physicists seeking a small set of rules to predict the behavior of the universe, or mathematicians developing the right language to precisely represent the defining features of problems.

This discussion gives us a framework to predict what problems LLMs would be good at solving, and where they would benefit from external help, tooling, and verification of their output.
To multiply large numbers, LLMs would generally do best to write a traditional computer program, rather than reason through the problem directly.
LLMs would be able to recall the name of a bone in the human body pretty easily and fairly accurately.
LLMs can decompose problems, but especially if the problem is fundamentally new with little available data on how to solve this problem “type”, human guidance will likely produce better results, and it is a good idea to write a checking procedure to catch any accuracy issues.
Nonetheless for problems like listing bones with suffix “-oid”, how to decompose this style of questions is well-known, and LLMs will still do well by leaning on their memory of what process to follow.
In data-rich domains, e.g., software development, it is possible that LLMs compensate for lower decomposition and abstraction abilities with superior memory compared to humans.

All four types of reasoning play off each other.
*Abstraction* is most powerful when one has *memory* of many objects to compare and draw abstract analogies between.
*Decomposition* is especially useful when some pieces can be solved *algorithmically*, some others by *remembering* the answer to the sub-question, and yet others by noticing that sub-question has common features with another one that you know how to solve as they both can be described by the same *abstraction*.
A significant strength of LLMs is that they show some ability to perform operations across all four domains.
Humans have experienced drastically improved problem-solving ability as we build tools that compensate for the areas where we are weakest.
Similarly, for problems that LLMs struggle with but that humanity cares about automating, building the *tools* that compensate for their weaknesses, will likely be an interesting area of research.
Combining the strengths of symbolic AI and LLMs in this way would result in *intersymbolic AI*, a solving paradigm that can achieve the best of both worlds.

_Acknowledgements: We thank André Platzer for feedback on this article._