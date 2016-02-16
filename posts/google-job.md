date: 2014-03-09

# Job at Google in 6 months recipe

**TL;DR** Read three books, watch two classes, solve problems at
topcoder/codeforces/projecteuler. Links are below.

If you are interested in getting a job at Google, you've probably already read
Steve Yegge's
[famous post](http://steve-yegge.blogspot.ch/2008/03/get-that-job-at-google.html)
(if you didn't, read it first).
It assumes you have only a couple of weeks for preparation and focuses on topics.
I used it as a checklist.
This recipe focuses on resources; depending on your background, requires 3-6
months, and gives you pretty good chances to pass the interview even if you
never knew the difference between a graph and a hash table.

After following the recipe you will

* have basic math, algorithm and data structure knowledge required for the
  interview
* change the way you think about problems, expressing them using mathematical
  models (it is not scary, rather fun)
* possibly love learning. Here at Google it is a continuous process and not less
  intensive.
* learn nothing about system design (see below)

I spent 2/3 of time on education and 1/3 on solving problems, but that's because
I had almost zero CS knowledge. If you just need a refresher, you should
probably spend more time on problems.

## Learn math

* Watch MIT's [Mathematics for CS](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-042j-mathematics-for-computer-science-fall-2010/index.htm) video course
* Read [course notes](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-042j-mathematics-for-computer-science-fall-2010/readings/MIT6_042JF10_notes.pdf)
* Do homework

The lecturer, Prof. Tom Leighton, is just great. He gives simple real-life
examples that help understanding material easily. The course is designed for
undergraduate students.

## Learn algorithms and data structures

* Watch MIT's [Introduction to Algorithms](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-006-introduction-to-algorithms-fall-2011/)
  video course.
* Read [Introduction to Algoritms](http://www.amazon.com/Introduction-Algorithms-Thomas-H-Cormen/dp/0262033844)
  book by Cormen et al.
* Do homework
* Write algorithm and data structure implementations yourself. Write unit tests
* Skim through the second part of [Algorithm design manual](http://www.amazon.com/Algorithm-Design-Manual-Steve-Skiena/dp/0387948600)
  book by Skiena.
  It is a catalog of well-known algorithmic problems.
  The first part is not required since Introduction to Algorithms covers theory
  pretty well
* Optionally, skim through [Algorithms](http://www.amazon.com/Algorithms-4th-Edition-Robert-Sedgewick/dp/032157351X)
  book by Sedgewick. He covers 3-way-quicksort and has great illustrations

The _Introduction to Algorithms_ book is the primary source of knowledge in the
whole recipe. The video lectures mainly explain the material in the book, bring
some fun, but also present something not covered by the book.

The book is big, but according to Steve and reports available on the Internet,
not all knowledge presented in the book is required for the interview. At least
you should read the material covered by the lectures. I enjoyed reading more
because it turned out to be soo interesting.

I believe writing code after reading theoretical material is the only way to
memorize it and find real-life obstacles, not obvious from pseudocode. For
instance, Dijkstra's algorithm pseudocode initializes distance for all nodes in
the beginning. In practice it will cause unnecessary memory waste and it is much
more efficient to assign distance to a node on discovery. I wouldn't figure this
out without implementing it myself.

## Learn multi-threading

* Selectively read [Java concurrency in practice](http://www.amazon.com/Java-Concurrency-Practice-Brian-Goetz/dp/0321349601)
  book

I didn't have time to read it all, but Part I Fundamentals is worth reading even
if Java is not your language. You must be able to tell why a given piece of code
won't work multi-threaded and how to fix it.

## Solve problems

The second part of the recipe is simply solving algorithmic problems available
at contest sites, such as [TopCoder](http://topcoder.com) and
[Codeforces](http://codeforces.com). Solve as many problems as time permits. It
is OK to feel "I am stupid" when looking at a problem. I still have it, yet I've
got a job.

Two main languages for an interview are Java Python and Go.
Choose one and use it to solve all problems.

There is a plenty of interview problems posted on the Internet.
Here are some of them:

* The [Cracking the Coding interview](http://www.amazon.com/Cracking-Coding-Interview-Programming-Questions/dp/098478280X)
  book by CareerCup contains 150 questions that you should know how to answer
* CareerCup's [forum](http://www.careercup.com/page?pid=google-interview-questions)
  for interview questions
* Solve first 50 problems at [Project Euler.net](http://projecteuler.net)
* MIT's [Hacking a Google interview](http://courses.csail.mit.edu/iap/interview/materials.php)
* [LeetCode](http://oj.leetcode.com/problems/)

Problems at topcoder/codeforces are generally more difficult than published
interview problems, so make sure you know how to solve all interview problems
that you find.

## Learn system design

You will be asked system design questions for sure.
This recipe does not cover it.
I didn't prepare for system design and regretted.
If you have a book/course recommendation, please post in comments.

Good luck, but more importantly prepare for intensive self-development.
After getting the job you will find this material was just a tip of an iceberg.
