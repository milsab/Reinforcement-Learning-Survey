# Reinforcement-Learning-Survey
Here, I share what I learn in reinforcement learning and its utilization in recommender systems. First, I will list all sources that I found useful and what I learned from them. So, you can find all the stuff that I'm going to write here in the following resources with far better explanations. My purpose is just to summarize what I'm learning in reinforcement learning and its application in recommender systems.

# Table of Contents
1. [Resources](#resources)
2. [Introduction](#introduction)
3. [Planning](#planning)
4. [Multi-Armed Bandits](#multi-armed-bandits)
5. [Full RL](#full-rl)
6. [Value-Based Approach](#valu-based-approach)
7. [Policy-Based Approach](#policy-based-approach)
8. [Actor-Critic Approach](#actor-critic-approach)
9. [Model-Based Approach](#model-based-approach)
10. [Deep Reinforcement Learning](#deep-reinforcement-learning)
11. [Major RL Algorithms](#major-rl-algorithms)




## Resources
### Books
- [Reinforcement Learning: An Intruduction](http://incompleteideas.net/book/the-book.html)   
This is like a bible book in reinforcement learning by Richard Sutton and Andrew Barto. Richard Sutton is one of the most prominent scientists in the field of reinforcement learning. The book includes three main sections. The first section covers tabular reinforcement learning. Multi-Armed Bandits, Markov Decision Process, and methods like Dynamic Programming, Monte Carlo Sampling, and Temporal Difference have been explained thoroughly in this section. The second section covers methods that use function approximation. So, this section is related to what we call deep reinforcement learning. The third section has some discussion on RL from different perspectives like psychology and Neuroscience.
- [Grokking Deep Reinforcement Learning](https://www.amazon.com/gp/product/1617295450/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)   
It is a great book to understand major concepts of reinforcement learning and deep reinforcement learning. Like the first book, this book also covers both tabular RL and Deep RL. The author has tried to explain concepts in a very intuitive way by avoiding going deep into maths. However, all the necessary maths has been discussed completely and intuitively. One great point of this book is that it has explanations of many recent major deep RL algorithms. 
### Online Cources
- [Reinforcement Learning Specialization](https://www.coursera.org/specializations/reinforcement-learning)   
It is a specialization in Coursera offered by the University of Alberta that includes four courses. This is a very complete specialization. It starts from very basic concepts and gradually goes through advanced concepts. It is interesting that throughout the specialization there are several videos that different scientists other than the two main instructors talking about a variety of RL subjects. Some of these videos include the conversations between Richard Sutton and Andrew Barto about RL.
- [RL Course by David Silver](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ)   
It is a link to a series of lectures that have been taught by David Silver at the University of College London. David Silver is another prominent scientist in the RL field. The fun fact is that he was a student of Richard Sutton. Also, he is one of the research scientists in Google DeepMind who contributed to designing many state-of-the-art algorithms in reinforcement learning.
- [RL Cource at University of College London](https://www.youtube.com/watch?v=ISk80iLhdfU&list=PLqYmG7hTraZBKeNJ-JE_eyJHZ7XgBoAyb&index=3)   
It is another series of lectures that have been taught at the University of College London. The instructor is Hado Van Hasselt who also is a senior research scientist at Google DeepMind. He has had a major influence to introduce the [DDQN](https://dl.acm.org/doi/10.5555/3016100.3016191) algorithm in a paper called "Deep Reinforcement Learning with Double Q-learning".
- [Deep RL Course at Berkeley](https://www.youtube.com/watch?v=8jQIKgTzQd4&list=PLkFD6_40KJIwTmSbCv9OVJB3YaO4sFwkX&index=1)   
It is a Deep Reinforcement Learning course that has been taught by Sergey Levine at the University of California, Berkeley in 2017. There is another [lecture series](https://www.youtube.com/watch?v=JHrlF10v2Og&list=PL_iWQOsE6TfURIIhCrlt-wj9ByIVpbfGc&index=1) that he taught DRL in 2020. He has had a major influence to introduce many algorithms including [PER](https://arxiv.org/pdf/1511.05952.pdf) and [SAC](https://arxiv.org/pdf/1801.01290.pdf).
- [RL Course at Stanford](https://www.youtube.com/watch?v=FgzM3zpZ55o&list=PLoROMvodv4rOSOPzutgyCTapiGlY2Nd8u&index=2)   
This course, CS234: Reinforcement Learning, has been taught by professor Emma Brunskill at Stanford University in Winter 2019.
- [Deep RL Bootcamp](https://www.youtube.com/watch?v=qaMdN6LS9rA&list=PLCJPYIcPhgPAiiBjjVxi5St_lC_cXHFCK)   
It is a deep reinforcement learning Bootcamp that includes 13 lectures. There are different instructors who teach these lectures like Pieter Abbeel, Vlad Mnih, Chelsea Finn, Sergey Levine, etc.


## Introduction
*# todo*
## Planning
*# todo*
## Multi-Armed Bandits
*# todo*
## Full RL
*# todo*
## Valu-Based Approach
*# todo*
## Policy-Based Approach
*# todo*
## Actor-Critic Approach
*# todo*
## Model-Based Approach
*# todo*
## Deep Reinforcement Learning
*# todo*
## Major RL Algorithms

 - [DQN](https://www.nature.com/articles/nature14236): Deep Q-Network 
 - [DDQN](https://arxiv.org/pdf/1509.06461.pdf): Double DQN
 - [PER](https://arxiv.org/pdf/1511.05952.pdf): Perioritized Experience Replay
 - [GPS](http://proceedings.mlr.press/v28/levine13.pdf): Guided Policy Search
 - [DPG](http://proceedings.mlr.press/v32/silver14.pdf): Deterministic Policy Gradient Algorithms
 - [DDPG](https://arxiv.org/pdf/1509.02971.pdf): Deep Deterministic Policy Gradient 
 - [TRPO](https://arxiv.org/pdf/1502.05477.pdf): Trust Region Policy Optimization
 - [GAE](https://arxiv.org/pdf/1506.02438.pdf): Generalized Advanced Estimation
 - [PPO](https://arxiv.org/pdf/1707.06347.pdf): Proximal Policy Optimization
 - [A3C](https://arxiv.org/pdf/1602.01783.pdf): Asynchronous Advantage Actor-Critic
 - [ACER](https://arxiv.org/pdf/1611.01224v2.pdf): Actor-Critic with Experience Replay
 - [SAC](https://arxiv.org/pdf/1801.01290.pdf): Soft Actor-Critic
 - [TD3](https://arxiv.org/pdf/1802.09477.pdf): Twin Delayed Deep Deterministic
 - [Rainbow](https://arxiv.org/pdf/1710.02298.pdf)
 - [Unicorn](https://arxiv.org/pdf/1802.08294.pdf)
