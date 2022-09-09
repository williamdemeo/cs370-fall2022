## CS 370: Introduction to Artificial Intelligence (Section 103)

### SCHEDULE

The *tentative* lecture and homework schedule shown below is subject to change.  Students should return to this page often throughout the semester to keep aprised of modifications in the schedule or homework due dates.

The links in the last column point to the AI lectures at UC Berkeley on the same material.
The Berkeley course presented the material in different order than ours.

<!-- In case you want to watch all of the Berkeley lectures in their original order, I made -->
<!-- a [AI YouTube playlist](https://youtube.com/playlist?list=PL5FJyaC2WsVndQJI9QtEhIMG2w8pYLN9u) just for you! :) -->



| **Week** | **Date** | **Topic**                         | **Reading**      | **Homework**                             | **Project Due Dates** | **UCB Videos**                  | **UCB Notes**      | **Alternative Notes** |
|----------|----------|-----------------------------------|------------------|------------------------------------------|-----------------------|---------------------------------|--------------------|-----------------------|
| **1**    | 9 Sep    | [Intro to AI (UCB version)][]     | Ch 1             |                                          |                       | [Intro to AI (YouTube)][]       |                    | |
|          |          | [Agents and Environments][]       | Ch 2             | [HW 1][] Agents, due Fri 16 Sep 23:59    |                       |                                 |                    | |
| **2**    | 16 Sep   | [Uninformed Search][]             | 3.1--3.4         |                                          |                       | [Uninformed Search (YouTube)][] | [Note 1: Search][] | [Note 1 (Fa '18)][]|
|          |          | [Informed Search][]               | 3.5, 3.6         | [HW 2][] Search, due Fri 23 Sep 23:59    |                       | [Informed Search (YouTube)][]   |                    | |
| **3**    | 23 Sep   | [A* Search and Heuristics][]      | 4.1, 4.2         |                                          |                       |                                 | [Note 2: Local Search][] | |
|          |          | [CSP I][]                         | 6.1, 6.2         | [HW 3][] CSP, due Fri 30 Sep 23:59       | [Project 0][] **due** | [CSP I (YouTube)][]             | [Note 2: CSP][]    | |
| **4**    | 30 Sep   | [CSP II][]                        | 6.3--6.5         |                                          |                       | [CSP II (YouTube)][]            | [CSP applet][]     | |
|          |          | [Adversarial Search I][]          | 5.2--5.5         | [HW 4][] Games, due Fri 7 Oct 23:59      |                       | [Game Trees I (YouTube)][]      | [Note 3: Games][]  | [Note 3 (Fa '18)][]| 
| **5**    | 7  Oct   | [Adversarial Search II][]         | 16.1--16.3       |                                          |                       | [Game Trees II (YouTube)][]     | [Note 4: Nondeterministic Search][] | |
|          |          | [Markov Decision Processes I][]   | 17.1--17.3       | [HW 5][] MDP, due Fri 14 Oct 23:59       | [Project 1][] **due** | [MDP I (YouTube)][]             |                    | |
| **6**    | 14 Oct   | [Markov Decision Processes II][]  |                  |                                          |                       | [MDP II (YouTube)][]            |                    | |
|          |          | [Reinforcement Learning I][]      | Ch 22            | [HW 6][] RL, due Fri 21 Oct 23:59        |                       | [RL I (YouTube)][]              | [Note 5: Reinforcement Learning][] | |
| **7**    | 21 Oct   | [Reinforcement Learning II][]     | Ch 22            |                                          |                       | [RL II (YouTube)][]             |                    | |
|          |          | [Probability][]                   | 12.1--13.5       | [HW 7][] Prob, due Fri 28 Oct 23:59      | [Project 2][] **due** | [Probability (YouTube)][]       |                    | |
| **8**    | 28 Oct   | [Bayes Nets I][]                  | 13.1, 13.2       |                                          |                       | [Bayes Nets (YouTube)][]        | [Note 5: Bayes Nets][] | [Note 6 (Fa '18)][] |
|          |          | [Bayes Nets II][]                 | 13.3             | [HW 8][] Bayes Nets, due Fri 4 Nov 23:59 |                       | [BN: independence (YouTube)][]  |                    | |
| **9**    | 4 Nov    | [Bayes Nets III][]                | 13.4             |                                          | [Project 3][] **due** | [BN: inference (YouTube)][]     |                    | |
|          |          | Review for exam                   | [Jordan 2.1][]  (optional reading) |                        |                       |                                 |                    | | 
| **10**   | 11 Nov   | EXAM (scope: 9 Sep--28 Oct)       |                  |                                          |                       |                                 |                    | |
|          |          |                                   |                  |                                          |                       |                                 |                    | |
| **11**   | 18 Nov   | [Bayes Nets IV][]                 | 13.5             | [HW 9][]. HMM; due Wed 23 Nov 23:59      |                       | [BN: sampling (YouTube)][]      |                    | |
|          |          | [Decision Networks and VPI][]     | 16.5, 16.6       |                                          |                       | [Decision Networks (YouTube)][] | [Note 7: Decision Networks][] |
| **12**   | 23 Nov   | [Hidden Markov Models][]          | 14.2, 14,3       |                                          |                       | [HMM (YouTube)][]               | [Note 6: HMM][]    |  [Note 8 (Fa '18)][] |
|          | (Wed)    | [Particle filters][]              | 14.4, 14.5       | [HW 10][]. Particle filters; due Fri 2 Dec 23:59 |               | [Particle filters (YouTube)][]  |                    | |
| **13**   | 2 Dec    | [ML: Naïve Bayes][]               | 20.1, 20.2       |                                          |                       | [ML: Naive Bayes (YouTube)][]   |  [Note 9: ML][]    | |
|          |          | [ML: Perceptrons, Logit][]        | 19.6, 19.7       |                                          |                       | [ML: Perceptrons, Logit (YouTube)][] |               | |
| **14**   | 9 Dec    | [ML: Optimization][]              | 18.6.3, 18.8     |                                          | [Project 4][] **due** |                                 | [Note 10: Neural Nets][] | | 
|          |          | [ML: Neural Nets][]               | Ch 21            |                                          |                       | [ML: Neural Nets (YouTube)][]   |                    | |
| **15**   | 16 Dec   | ([final exams][] begin)           |                  |                                          |                       |                                 |                    | |
| **16**   | 24 Dec   | (final grades due)                |                  |                                          |                       |                                 |                    | |


----------------------

### Fall 2022 Academic Calendar

| **Date** | **Day** |   |
|--------|--------|---------------------------------|
| September	5 | Monday | Labor Day. University Closed |
| September	6 | Tuesday | First Day of Classes |
| September	12 | Monday | Last Day to Add/Drop a Class |
| September	12 | Monday | Last Day for 100% Refund, Full or Partial Withdrawal |
| September	13 | Tuesday | W Grades Posted for Course Withdrawals |
| September	19 | Monday | Last Day for 90% Refund, Full or Partial Withdrawal |
| October	3 | Monday | Last Day for 50% Refund, Full Withdrawal |
| October	24 | Monday | Last Day for 25% Refund, Full Withdrawal |
| November	14 | Monday | Last Day to Withdraw from Classes  |
| November	22 | Tuesday | Thursday Classes Meet |
| November	23 | Wednesday | Friday Classes Meet |
| November	24 | Thursday | Thanksgiving Recess Begins (No Classes) |
| November	26 | Saturday | Saturday Classes Meet |
| November	27 | Sunday | Thanksgiving Recess Ends |
| December	14 | Wednesday | Last Day of Classes |
| December	15 | Thursday | Reading Day |
| December	16 | Friday | Final Exams Begin |
| December	22 | Thursday | Final Exams End |
| December	24 | Saturday | Final Grades Due |







[final exams]: https://www5.njit.edu/registrar/exams/finalexams.php




[KUPF]: https://goo.gl/maps/GjhP3cjrMAJSzVFt5

<!-- LINKS TO LECTURE NOTES -->

[Note 1: Search]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/notes/n1_sp22.pdf
[Note 1 (Fa '18)]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n01-search.pdf
[Note 2: Local Search]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/notes/n2_sp22.pdf
[Note 2: CSP]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n02-csp.pdf 
[CSP applet]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/demos/csp/csp_demos.html
[Note 3: Games]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/notes/n3_sp22.pdf
[Note 3 (Fa '18)]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n03-adversarial-search.pdf
[Note 4: Nondeterministic Search]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n04-nondeterministic-search.pdf
[Note 4: Logical Agents]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/notes/n4_sp22.pdf
[Note 5: Reinforcement Learning]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n05-rl.pdf
[Note 5: Bayes Nets]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/notes/n5_sp22.pdf
[Note 6 (Fa '18)]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n06-bayes-nets.pdf
[Note 6: HMM]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/notes/n6_sp22.pdf
[Note 7: Decision Networks]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n07-decision-networks.pdf
[Note 8 (Fa '18)]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n08-hmm.pdf
[Note 9: ML]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n09-ml.pdf
[Note 10: Neural Nets]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/n10-neural-nets.pdf


<!-- Project LINKS -->
[Project 0]: https://github.com/williamdemeo/cs370-fall2022/tree/master/projects/Project0
[Project 1]: https://github.com/williamdemeo/cs370-fall2022/tree/master/projects/Project1
[Project 2]: https://github.com/williamdemeo/cs370-fall2022/tree/master/projects/Project2
[Project 3]: https://github.com/williamdemeo/cs370-fall2022/tree/master/projects/Project3
[Project 4]: https://github.com/williamdemeo/cs370-fall2022/tree/master/projects/Project4



<!-- HW LINKS -->

[HW 1]: https://www.gradescope.com/courses/361553
[HW 2]: https://www.gradescope.com/courses/361553
[HW 3]: https://www.gradescope.com/courses/361553
[HW 4]: https://www.gradescope.com/courses/361553
[HW 5]: https://www.gradescope.com/courses/361553
[HW 6]: https://www.gradescope.com/courses/361553
[HW 7]: https://www.gradescope.com/courses/361553
[HW 8]: https://www.gradescope.com/courses/361553
[HW 9]: https://www.gradescope.com/courses/361553
[HW 10]: https://www.gradescope.com/courses/361553
[HW 11]: https://www.gradescope.com/courses/361553


<!-- LINKS TO UCB LECTURE YOUTUBE VIDEOS -->

[Intro to AI (YouTube)]: https://www.youtube.com/watch?v=16Dir4QqCUg
[Uninformed Search (YouTube)]: https://youtu.be/-Xx0QSFYfIQ
[Informed Search (YouTube)]: https://youtu.be/Mlwrx7hbKPs
[CSP I (YouTube)]: https://youtu.be/81z2ANjQcH4
[CSP II (YouTube)]: https://youtu.be/_DXf6oaknHw
[Game Trees I (YouTube)]: https://youtu.be/v6RgZBjc8og
[Game Trees II (YouTube)]: https://youtu.be/n3A29GEzC6g
[MDP I (YouTube)]: https://youtu.be/4LW3H_Jinr4
[MDP II (YouTube)]: https://youtu.be/ZToWj64rxvQ
[RL I (YouTube)]: https://youtu.be/TiXS7vROBEg
[RL II (YouTube)]: https://youtu.be/XafrqwHfBKE
[Probability (YouTube)]: https://youtu.be/sMNbLXsvRig
[Bayes Nets (YouTube)]: https://youtu.be/T4l6ltMMcec
[BN: independence (YouTube)]: https://youtu.be/FUnOdyZZAaE
[BN: inference (YouTube)]: https://youtu.be/A1hYXGAUdmU
[BN: sampling (YouTube)]: https://youtu.be/kGngCS-1kjU
[Decision Networks (YouTube)]: https://youtu.be/19sr7yKV56I
[HMM (YouTube)]: https://youtu.be/eCZLhZu_U1I
[Particle filters (YouTube)]: https://youtu.be/pNam9hbwg4g
[ML: Naive Bayes (YouTube)]: https://youtu.be/1nOb0vwWkAE
[ML: Neural Nets (YouTube)]: https://youtu.be/LERtLI2h_nQ
[ML: Perceptrons, Logit (YouTube)]: https://www.youtube.com/watch?v=UNr9gHyOnWA
[ML: Decision Trees (YouTube)]: https://youtu.be/svW3I0cqfpw
[Robotics (YouTube)]: https://youtu.be/MxS1aYvYNNc

<!-- LINKS TO LECTURE SLIDES -->
[Intro to AI (UCB version)]: https://inst.eecs.berkeley.edu/~cs188/sp22/assets/slides/Lecture1.pptx
[Agents and Environments]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec02-AgentsAndEnvironments.pptx
[Uninformed Search]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec03-Search.pptx
[Informed Search]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec04-InformedSearch.pptx
[A* Search and Heuristics]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec05-AstarSearchAndHeuristics.pptx
[CSP I]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec06-CSP-I.pptx 
[CSP II]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec07-CSP-II.pptx
[Adversarial Search I]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec08-AdversarialSearch-I.pptx
[Adversarial Search II]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec09-AdversarialSearch-II.pptx
[Markov Decision Processes I]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec10-MDP-I.pptx
[Markov Decision Processes II]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec11-MDP-II.pptx
[Reinforcement Learning I]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec12-RL-I.pptx
[Reinforcement Learning II]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec13-RL-II.pptx
[Probability]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec14-Probability.pptx
[Bayes Nets I]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec15-BayesNets-I.pptx
[Bayes Nets II]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec16-BayesNets-II.pptx
[Bayes Nets III]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec17-BayesNets-III.pptx
[Bayes Nets IV]: https://github.com/williamdemeo/cs370-fall2022/raw/master/lecture/slides/CS370-Lec18-BayesNets-IV.pptx
[Logical Agents]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[Inference in First Order Logic]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md

[Decision Networks and VPI]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/slides/CS370-Lec19-DecisionNetworks.pptx
[Hidden Markov Models]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/slides/CS370-Lec20-HMM.pptx
[Particle filters]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/slides/CS370-Lec21-HMM-II.pptx
[ML: Naïve Bayes]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[ML: Perceptrons and Logistic Regression]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[ML: Perceptrons, Logit]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[ML: Optimization]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[ML: Neural Nets]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[Advanced Applications: Games and Robotics]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md
[Conclusion]: https://github.com/williamdemeo/cs370-fall2022/blob/master/lecture/dne.md

<!-- MISC LINKS -->
[Jordan 2.1]: https://github.com/williamdemeo/cs370-fall2022/tree/master/notes/chapter2.pdf
[KUPF 202]: https://goo.gl/maps/GjhP3cjrMAJSzVFt5
[edX AI wk10: Logical Agents]: https://learning.edx.org/course/course-v1:ColumbiaX+CSMM.101x+2T2018/home






<!-- [Note 1]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note01.pdf
[Note 2]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/note02.pdf>
[Note 3]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note03.pdf
[Note 4]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note04.pdf
[Note 5]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note05.pdf
[Note 6]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note06.pdf
[Note 7]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note07.pdf
[Note 8]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note08.pdf
[Note 9]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note09.pdf
[Note 10]: https://inst.eecs.berkeley.edu/~cs188/fa21/assets/notes/fa20-note10.pdf
-->