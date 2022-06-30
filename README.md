# Reinforcement Learning Survey
Here, I share what I learn in reinforcement learning and its utilization in recommender systems. First, I will list all sources that I found useful and what I learned from them. So, you can find all the stuff that I'm going to write here in the following resources with far better explanations. My purpose is just to summarize what I'm learning in reinforcement learning and its application in recommender systems.

# Table of Contents
1. [Resources](#resources)
2. [Basic Concepts of Reinforcement Learning](#basic-concepts-of-reinforcement-learning)
3. [Markov Decision Process](#markov-decision-process)
4. [Planning](#planning)
5. [Multi-Armed Bandits](#multi-armed-bandits)
6. [Full RL](#full-rl)
7. [Value-Based Approach](#valu-based-approach)
8. [Policy-Based Approach](#policy-based-approach)
9. [Actor-Critic Approach](#actor-critic-approach)
10. [Model-Based Approach](#model-based-approach)
11. [Deep Reinforcement Learning](#deep-reinforcement-learning)
12. [Major RL Algorithms](#major-rl-algorithms)




## Resources
Before I jump in to summarize my understanding of reinforcement learning, I decided to put the resources at the beginning because everything I will describe here has been explained in a so much better way in the following resources.
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


## Basic Concepts of Reinforcement Learning
Reinforcement Learning (RL) is a type of machine learning that which the task of learning is based on trial and error. We have an agent who interacts with the environment. In each interaction, the agent takes an action on an environment. The environment reacts to that action by providing feedback. Also, the environment may change its current state to a new state. In RL, the feedback is a scalar value that represents how much the action which was taken by an agent was good in regard to the final goal.  In a nutshell, we have the following basic concepts in any RL problem.

#### Environment
It is a problem that we want to solve. Usually, a problem may have a different state and we want to find a way (policy) that guides us from any given state to a final or a goal state. For example, in recommender systems, if we want to capture the dynamics of user behaviors, the environment will be the user.  

#### Agent
It is a learning program that tries to learn how to take an action in an environment in order to reach a final goal. For example, in recommender systems, the agent is the recommendation engine that tries to recommend items to users that align with users' preferences in order to increase user satisfaction in the long run. 

#### State
An environment may have different states. There is a sub-category of the RL problems that the environment has only one state. In this type of RL problems, the state of the environment is stationary. This type of RL problems is called Multi-Armed Bandits problems that I will discuss in more detail later. Each state can be represented by a set of variables. State space can be discrete or continuous.
#### Observation
The part of the state that an agent can observe is called observations. Each environment has a set of states. Some agents can see the entire state set of an environment, while some agents can observe only a subset of states.  

#### Action
An agent has access to a set of actions that can take on an environment. For example, in a recommender system, action is recommending an item or a list of items to a user. Action space can be discrete or continuous.
#### Transition Function 
It is a function that maps an action to a state. 
#### Reward Function
It is a function that generates a scalar value based on the action that has been taken by an agent on an environment. The scalar value is called reward. Reward indicates how good or bad the action was. If an action helps the agent to reach a goal state in an environment, the agent receives a high reward. Otherwise, the agent may receive low rewards or no rewards at all. Sometimes an agent may receive a negative reward based on an application domain and the design of the system. Defining an appropriate reward function is very important to design an RL-based system.

#### Return
Return is the summation of all rewards that an will receive from a current state to a final state.

#### State-Value Function
Expected reward from current state to a final state. 
#### Action-Value Function
If we are at a current state and take an action, the action-value function will be the expected reward from that state to a final state taking that action.
#### Model
A set of transition function and reward function is referred to as a model of an environment. In fact, if we have access to the transition function and reward function of an environment, then, we have access to the model of that environment. In many real-world problems, we do not have access to both the reward function and transition function so, the model of the environment is unknown. There are many RL algorithms that try to find the best way to reach the goal state in an environment by considering the fact that they do not have access to the model of that environment. They are called model-free algorithms.
#### Policy 
There are different ways or strategies that an agent can go from a given state in an environment to a goal state. In RL, the term that uses to describe each of those strategies is called policy. Based on a policy, an agent can take an action according to the current state. In other words, a policy is a mapping from the state (observation) to an action. The final goal of any agent is to find an optimal policy that guides the agent to reach the goal state in the best optimal way. If an agent tries to learn an optimal policy by directly learning policy, it calls a policy-based agent. There are other types of agents like value-based agents and actor-critic agents which are somehow a combination of policy-based and value-based agents.
#### Episode
An episode is a path that an agent starts from a start state or any other given state and ends in a final state. A final state may or may not be a goal state. An environment may have several start sates and final states. Some of those final states can be goal states. The agent's task is to interact with an environment and learn how to find the best policy to reach the goal. If an agent's task ends naturally it is an episodic task, otherwise, it is a continuous task.

## Markov Decision Process
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
## Major Deep Reinforcement Learning Algorithms
The below list is linked to some of the most influential papers that have introduced major reinforcement algorithms. Some of them like DQN and DDQN are value-based methods and some of them like DDPG and TRPO are policy-based methods. Others like A3C, TD3, and SAC are actor-critic methods.
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
