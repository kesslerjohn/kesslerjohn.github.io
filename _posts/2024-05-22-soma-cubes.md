---
title:  "Making a Wooden Soma Cube Puzzle"
date: 2024-05-22
permalink: /posts/2024/05/soma-cubes/
tags:
  - hobbies
  - woodworking
  - recreational mathematics
  - puzzles
---
This idea came to me from a book of puzzles written by Martin Gardner in the late 20th century. _TODO: Give book name/link if possible._ The puzzle is made up of 7 pieces - the first of which is composed of 3 cubes, while the remaining 6 are each composed of four cubes. Gardner provides a handy illustration of the puzzle pieces:

------

![gardners_book](https://github.com/kesslerjohn/kesslerjohn.github.io/assets/80122119/f5660283-e2da-461b-a65d-96284f14f9da)

------

I used this as a guide to make my copy of the puzzle. I also needed some wooden blocks, and my local antiques store came through! I found a nice bag of wooden blocks with (mostly) uniform size and design for just \\$6, tax included. 

------

![cubes-bag](https://github.com/kesslerjohn/kesslerjohn.github.io/assets/80122119/e1845d51-4ffb-44c7-bd4f-0fe96e2b3571)

------

Before you say I got ripped off, this bag holds 48 red cubes, 3/4" on an edge, with numbered faces! (plus two slightly smaller blue cubes, also with numbered faces). A set of 27 3/4" wooden cubes at Lowe's would have cost me around \\$10 - and those don't have numbered faces. 

So what's the big deal about numbered faces? It's not a compromise to buy these cubes, because the numbers give me the opportunity to add another level of curiosity to the puzzle; after all, there's a lot you can do with numbers [citation needed]. One thing you can do is add them together, so I thought I would try adding them to make prime numbers; I would arrange the cubes so that the sum of the visible faces on each Soma piece would be a prime number. 

My first approach was to do this by hand, by drawing out a mesh for each cube (there are two kinds - one has faces numbered 0-5, and the other is numbered 5-10). 

[meshes image here]

I had originally planned to only use the blocks with low-numbered faces, but I realized that if I messed up a block in the process of making the cubes, I wouldn't have enough replacements. So I needed to balance the number of low-valued and high-valued cubes I included. At this point, the number of possible configurations for each cube was becoming overwhelming, and the brute-force approach was too taxing to undertake by hand. 

I resolved this by writing a program to brute-force it for me. The code is available in [this repository]. The program looks at all the choices for 4 cubes, and all possible ways to hide a given number of faces (usually 2 per cube, but in piece 7, the middle cube has 3 hidden faces), and prints out the configurations for which the non-hidden faces sum to a prime number. From this output, I could freely choose configurations that used a balanced number of low- and high-value cube faces.
