---
layout: post
title:  "Literature Reviews"
# date:   2019-04-29 12:37:06 -0400 # Still a draft!
categories: literature
---

#### This is a draft. I will keep appending, but publishing now anyway so I have incentive to complete and because no one's going to land here anyway lol

As a beginning researcher, something I have had to do often is literature reviews. Whether I'm to track down all relevent existing work at the start of a new project, or am trying to find answers to a specific question that I know had to have been answered at some point in the past, I find myself requiring the ability to effectively search through the existing body of academic work.
<!-- It's one of the things that I was rather bad at to begin with, that I was never taught how to do right in classes.  -->
This post is intended for the benefit of those who find themselves in the same place I was an year ago- faced with the task of having to search through dense literature in a field they are not familiar with, sans guidance, with no idea where to start.

I'm going to present through examples how I go about searching for relevent papers. 
First, I attempt to perform a broad field review in an area I have no familiarity with- mathematical sociology. My objective is to identify seminal papers and get a rough feel for the shape of the field. 
In the second example, I search for a specific piece of information- the exact reduction of the computation of the Hafnian fo a matrix to a classic sharp-P complete problem (more context on this later), assuming that I have no familiarity with the existing literature of complexity theory and only an undergrad's course-based understanding of the field.

Disclaimer: This article is based on the tricks I've picked up through trial and error over the course of my limited experience in research. I'm sure there's a lot I don't know, so if you have suggestions/advice, I'd love to hear it!

## Surveying a Field

I aim to survey mathematical sociology, starting off with only the vague notion that sociology is the study of society and using math to formalize it might be interesting. The objective is to get a rough sense of the main ideas in the field. 
I need to find a starting point to jump in, so I pay a visit to the hallowed halls of [Wikipedia](https://en.wikipedia.org/wiki/Mathematical_sociology).
<!-- I also search "mathematical sociology survey" on google scholar. -->

Skimming through the History section, the first mentioned work that strikes me as interesting is the graph formalism be Frank Harari that "produced the fundamental theorem of this theory".
Conveniently, Wikipedia [cites the paper in question](https://en.wikipedia.org/wiki/Mathematical_sociology#cite_note-5)- Cartwright, Dorwin & Harary, Frank. (1956). "Structural Balance: A Generalization of Heider's Theory." Psychological Review 63:277-293.
I head to my University Library's website and get the pdf (conveniently, my credentials still work though I've graduated a few months ago).

I go over the first few pages to get the groundwork and then start skipping, looking for the central results. I'm rewarded with the section "STATEMENT OF THE PROBLEM" and later, the italicized phrases- the theorems in "SOME THEOREMS ON BALANCE", terms in "FURTHER CONCEPTS IN THE THEORY OF BALANCE" and so on. I decide this paper is interesting and that I probably want to return and read it properly later.

As a quick aside, I run a Google scholar search of all the articles that cite "Structural Balance: A Generalization of Heider's Theory". There are over 2000 results, ordered roughly by citations ("sort by relevance"), with such a broad search I'm just going to glance at the first two pages. Unsurprisingly the papers lie in a large spectrum, from psychology to natural language processing, but a some results strike me as useful- J Scott's "Social Network Analysis", the first result, seems like a great survey paper. "Network Analysis" by D Knoke and JH Kuklinski, "Structural equivalence of individuals in social networks" by F Lorrain and HC White, and "From Factors to Actors: Computational Sociology and Agent-Based Modeling" by MW Macy and R Willer look like they may belong to my reading list too. I'm sure there's a lot more, varied content to be found on later search pages, but I want to return to Wikipedia for now.

Next Wikipedia talks of progress on mathematical process, and presents [The Human Group](https://en.wikipedia.org/wiki/Mathematical_sociology#cite_note-6) as an example. I once again look this up, it seems to be a book. I can't find a version I can access for free online, so at the moment I'll pass. Maybe I'll come back and look at works that cite it instead later.

Moving on, I go through the "Further Developments" section, and can apply the same process to identify the papers that were seminal. I'm not actually going to that yet because I'm feeling lazy. I rationalize that the works in question would still only historical context relative to current research.
The next section tells me of "such central journals as [The American Journal of Sociology](https://www.journals.uchicago.edu/toc/ajs/current) of Sociology and [The American Sociological Review](https://journals.sagepub.com/home/asr)" and most of all, "[The Journal of Mathematical Sociology](https://www.tandfonline.com/loi/gmas20)". This is very useful information, I can peruse the abstracts of the more recent volumes and get a sense of what's going on in the field currently. If there are particularly intriguing abstracts make no sense to me, I can "[climb up the citation tree](#citationTree)" till I understand them. But I refrain from doing that just yet, because Wikipedia's next section, "[Research programs](https://en.wikipedia.org/wiki/Mathematical_sociology#Research_programs)" gives me the perfect way to identify an organized set of papers to get an overview of the more important threads of study on the field.

I will do this analysis for only one of the 9 "programs" described, leaving the rest of the analysis as an [exercise to the reader](https://aditink.github.io/satisfying/).
So my task is now to look at Structuralism. The first thing wikipedia mentions is a book, Chains of Opportunity: System Models of Mobility in Organizations. However a Google scholar search revelas the same author published an article the same year, so I'm guessing it's closely related. A look at the article confirms the hypothesis.
The process is repeated for the rest of the papers/articles mentioned in the paragraph.
I now proceed to find more recent citations of these papers in google scholar, as I had done with "Structural Balance: A Generalization of Heider's Theory". I identify papers with particularly high citation counts and add them to my reading list.
I now have a decent number of papers, but given that I have finite time, I pick and choose how much of each I want to read with the objective of grasping the central idea.
At the end, I think I have a rough idea of what the discipline is about.

The subject of this case study turned out to be unusual in that I could rely on a central guiding resource, Wikipedia. This will often not be the case, nevertheless I ended up using ideas and methods that would allow you to survey the field regardless.

* We need a starting point. 

   There are many ways to find starting points- a google search that leads you to a survey paper or a textbook, or a summary page for example. In each of these cases you can apply the method of looking up the papers corresponding to the introduction of the important ideas mentioned, as we did here. Or perhaps you know of the important journals or conferences in the field, or even of just an important paper, or of a Professor with papers in the area? If this is the case then you go backwards in time, looking at the important papers cited by your starting paper(s), and then the papers cited by them, and so on, till you reach the point where the important foundational ideas of the field are being introduced.

* We need to travel from the starting point to the *important* papers. 

   Already spoke a bit about how to do this in the previous point, but the idea is that if you read only recent, specialized work, it'll be dense and jargon-ey, and you probably won't cover as much conceptual ground. Think of the literature of a field like a tree. There are root papers that inspire child papers, and the most recent papers are leaf nodes. The objective is to traverse the tree in such a way as to get a decent idea of it's general shape, and conceptual understanding of its trunk and thickest branches so that you have the context to comprehend even the leaf nodes. You can climb both up and down a tree, so it's a tree traversal problem. If you start close to the leaves, you go back to an ancestor, and then look at its most important children. If you start at the root, you do the opposite, and look for successor papers.

* We need to figure out which papers are important and actually read them.

   Firstly, abstract and citation count are good indicators of importance.
   There is bound to be redundancy in your search, so it might make sense to make a quick fist pass on papers and then decide which details to read. In fact, depending on your objective, it's often ok to focus on the exact things you were looking for (central idea, a specific theorem, methodology used, etc) and let the details fade away.
   Finally, when there's assumed background knowledge that makes a paper to be incomprehensible, Googling and reading cited work often helps a lot.

#### Climbing the Citation Tree <a name="pookie"></a>
This is really simple. Going back to the tree analogy, to climb "up" the paper tree, towards the root, look at the papers cited for the fundamental underlying concepts in the work. These papers are the predecessor nodes of the current paper. You look them up and repeat the process as often as required to climb the citation tree. The reverse can also be done- you can descend down the tree by looking at the important articles that cite the current paper using the Power of Modern Search Engines.

## Finding Specific Information

I'll write this later, but it's really about keywords and more citation tree climbing.