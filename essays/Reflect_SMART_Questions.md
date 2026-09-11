---
layout: essay
type: essay
title: "So Akamai"
# All dates must be YYYY-MM-DD format!
date: 2026-09-10
published: true
labels:
  - Computer Science
---

<img width="200px" class="rounded float-start pe-4" src="../img/difficulty/degree_difficulty.jpg">

## Why Smart Questions Matter
Note: CHATGPT was used to polish my work slightly by helping with grammar and formatting. 
  Software engineering is often described as a technical discipline, but technical knowledge alone is not enough to become an effective software engineer. Programmers spend a significant amount of time communicating with other people: teammates, users, documentation authors, maintainers, and online communities. One of the most important forms of this communication is asking for help. A programmer may have excellent technical ability but still waste considerable time if they cannot explain a problem clearly enough for another person to understand and reproduce it.

  Eric Raymond's essay, How To Ask Questions The Smart Way, provides a useful framework for thinking about this problem. Raymond argues that the quality of the answer someone receives depends significantly on the quality of the question. His recommendations include doing research before asking, describing the problem precisely, reporting relevant symptoms rather than assumptions, providing enough information to reproduce the problem, stating the desired result, and making the question easy for another person to answer. 

  Stack Overflow provides an excellent environment for seeing these principles in practice. The contrast between a well-constructed question and a poorly constructed one demonstrates that asking questions is itself a technical skill. The two questions examined below show how the amount and organization of information supplied by the questioner can directly affect the efficiency and usefulness of the community's response.

## What Exactly is a Smart Question?

  Raymond's central idea is that asking for technical help should not be treated as simply demanding that somebody else solve a problem. Before asking, a programmer should search existing resources, experiment, inspect documentation, and attempt to isolate the problem. When the question is finally posted, the question should demonstrate this effort. Raymond specifically recommends being precise and informative, describing symptoms rather than guesses, explaining the desired outcome, and providing a reproducible example when code is involved. 

  These principles are also reflected in Stack Overflow's own guidance. Stack Overflow recommends explaining how the problem was encountered, describing difficulties encountered while trying to solve it, and providing enough code for others to reproduce the problem. It specifically warns against simply posting an entire program containing large amounts of irrelevant material. 

  A smart question therefore reduces the amount of work required from the person answering it. Instead of making an expert reconstruct the entire situation, the question provides the relevant facts up front. This does not mean that a good question must be long. In fact, a good question can be quite short if it contains the right information.

# Case Study Not-So-Smart Question 

URL: [StackOverFlow](https://stackoverflow.com/questions?tab=newest&page=1609263)

The Stack Overflow question "extract duplicate characters from a string" is a strong example of a question that does not follow Eric Raymond's guidelines for asking questions the smart way. The question was posted by a beginner asking for help with a JavaScript homework assignment. The author explains that they need to extract duplicate characters from a string and put them into another string. They provide the example "love to learn javascript" and state that the resulting string should be "love tarnjscip". However, the author also explicitly says, "I didn't made any try as I'm a beginner and I don't have an initial idea how to start."

This question is particularly interesting because the problem is not simply that the author is a beginner. Beginners are absolutely encouraged to ask questions. The larger problem is that the author has not yet attempted to solve the problem or sufficiently clarified what the desired result actually means. These issues conflict with several of Raymond's recommendations.

One of Raymond's most important recommendations is to try to solve the problem before asking someone else for help. He argues that a question should demonstrate that the person asking has made a reasonable effort to investigate the problem. In this case, the author openly states that they have made no attempt to solve the problem. They speculate that a nested loop might be necessary, but they do not show any code or explain what they tried. Furthermore, several characters in that output occur only once in the original string. This ambiguity was noticed by multiple answerers. One commenter specifically points out that the result contains characters that were used only once. Another answerer acknowledges that the description and example do not really match. This is a major violation of the principle of being precise. A programmer trying to answer the question has to determine what the author actually means before determining how to solve it.

At the same time, the question did receive five answers, so it would be inaccurate to claim that asking a question this way produces no useful help. In fact, the community provided several useful solutions. The better conclusion is that the question produced less efficient and less focused help than it could have. The answerers had to compensate for shortcomings in the original question.

That distinction fits the purpose of the assignment particularly well. Raymond's principles do not guarantee that a smart question will receive a good answer or that a poorly written question will receive no answer. Instead, they help maximize the likelihood that other programmers can understand the problem quickly and provide an answer that addresses the questioner's actual difficulty.

This example therefore demonstrates an important lesson: the responsibility for communicating a programming problem clearly belongs primarily to the person asking the question. If the programmer has not determined what the expected behavior actually is, has not attempted a solution, and cannot explain where the attempt failed, the people trying to help must first solve the communication problem before they can solve the programming problem.

For a software engineer, learning to avoid this situation is valuable. The process of defining the expected behavior, attempting a solution, identifying the failure, and communicating that failure precisely is not just good Stack Overflow etiquette—it is good software engineering.


# Case Study: Smart Question 





# Why This Matters for Software Engineers and Insights 

Smart questions matter because software development is rarely an individual activity. Even when a programmer is working alone, they depend on documentation, libraries, open-source projects, search engines, colleagues, and developer communities. The ability to communicate a problem efficiently therefore directly affects productivity.

A poorly constructed question transfers unnecessary work to the person being asked for help. The answerer must first determine what the problem actually is, what the desired behavior should be, what environment is involved, and which portions of the code matter. Sometimes the answerer has to ask several follow-up questions before meaningful debugging can begin.

A well-constructed question performs much of this work in advance.

This does not mean that inexperienced programmers should avoid asking questions. Raymond's essay is not an argument that beginners should already know everything. Rather, it encourages beginners to demonstrate that they have made a serious attempt to understand the problem. Raymond argues that good questions can be interesting and valuable to the community because they stimulate understanding and can reveal problems that others have not noticed. 

There is also a long-term benefit. A programmer who learns to formulate a reproducible example, identify expected versus actual behavior, check documentation, and report relevant environmental information is also learning how to debug. The skills required to ask a smart question are closely related to the skills required to solve a problem independently.

# Conclusion 

The most important insight I gained from comparing these questions is that the quality of a question is partly determined by how much uncertainty it removes for the person answering it.

Before this comparison, it would be easy to think that a "good question" simply means being polite and providing a lot of code. The examples show that neither is sufficient. The Seaborn question is effective not because it is long, but because almost every piece of information has a purpose. The matrix, code, expected behavior, actual behavior, library versions, and research information all help narrow down the possible explanation.The Java question demonstrates the opposite. More code does not necessarily make a question better. A programmer can provide an entire program and still leave the most important question unanswered: What exactly is going wrong?I also learned that a minimal reproducible example is more than a Stack Overflow rule. Creating one is a practical debugging technique. If I cannot reduce a problem to a small example, I may not yet understand which part of my program is actually responsible for the problem.Finally, I learned that smart questions respect the time of the people providing help. Online technical communities consist of people who are volunteering their knowledge. Providing a focused question does not guarantee an answer, but it makes it substantially easier for someone knowledgeable to investigate the problem. It also makes the resulting answer more useful to future programmers who encounter the same issue.

  
