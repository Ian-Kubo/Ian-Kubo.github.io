---
layout: project
type: project
image: img/webscrape.png
title: "Something Fishy"
date: 2026
published: true
labels:
  - Lisp
  - GitHub
summary: "A Simple Fishing Game Developed for ICS211."
---

<img class="img-fluid" src="../img/cotton/cotton-header.png">

  Something Fishy is a two-person, turn-based fishing game that will definitely have you hooked! The goal of this game is to compete throughout the fishing season to--simply put it--fish! The "pond" contains varying fish population densities, and it is your job that your basket contains the largest fish. At the end of the season, the three largest catches from each payer are weighted, and the person with the highest average weight wins. 

  Get your tools out and reel in some fresh catches!

  ## Game Details 
  This game is a 12-month (in-game)  competitive fishing tournament where players compete to catch the largest fish. At the start of each month, the fishpond is randomly populated with different indigenous fish. Smaller fish appear closer to the shore, while larger fish are more available in deeper waters. Players can observe the pond with varying levels of detail depending on distance- nearby fish are clearly visible while fish appear as shadows in murky waters, and fish in the deepest waters provide no information at all. Each player gets five actions per month, alternating turns, and can either spend an action to view pond information or cast a fishing line.
When casting, players choose both a location and whether to use a previously caught fish as bait. Bait affects gameplay because fish have a chance to notice it, with the Oama species being more attractive than standard bait. Once a fish is triggered, a random outcome determines what happens next, with possible results including a successful catch, the line snapping, or even hooking unwanted items like garbage. If a fish is caught, the player must decide whether to keep it. Legal fish can be stored in the player’s inventory, while illegal catches result in penalties, adding a risk-reward element to every decision.
  At the end of each month, the cycle resets with a fresh population of fish and renewed turns for both players. This continues for 12 months in total, creating a long-term strategy game where players must balance risk, timing, and bait usage. The winner is determined at the end of the year by weighing the three largest fish each player has kept. The player with the highest total weight from their top three catches is declared the champion of the tournament!

  Link to source code

## Diving Deeper
  Visual Studio Code was used as our primary Integrated Development Environment (IDE), and it’s built in AI friend, Copilot, helped streamline our game development. More specifically, the use of AI gave us insights on how to better improve certain code segments and reduced the number of redundant code, acting like a proofreader on our project. Furthermore, we used the Java language to create this game. Since Java is object-oriented by design, it was highly intuitive to model real world entities within this language. We created an abstract I’a superclass that defined a specific fish behaviors such as their growth stage, diet, reproduction, size and weight, and sex and color change. These traits were then inherited by its subclasses, which were modeled by several different Hawaiian fish types, each with unique traits. 
  Since this project was accomplished by teams of three, we broke down the project into thirds. My two other teammates handled UI design and the "season" mechanics, ultimately adding up to one complete game. My primary role for this project was developing algorithms for the fishing mechanics. I used switch statements to create different fishing scenarios and a heap to act the player's inventory. 
  This project helped me better understand several CS related topics. First off, we collaborated using Github. This taught me how to clone repositories, use branching for work, and commit and push projects onto the repository. Using Github also helped me better develop my soft skills of communication and collaboration within a team. In terms of programming, the game was made to hone our knowledge on basic data structures and algorithms and object-oriented programming. Creating a fun but complex project helped me have a deeper understanding on topics such as abstract classes, interfaces, and heaps in Java. Overall, creating this game with my team was extremely beneficial in my journey as a software engineering. Our finale consisted of presenting this project to an undergraduate research fair: here's the poster!


