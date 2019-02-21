# Auto ML: Literature Review 
The sole objective of this venture is to be able to create a framework that lets non ML users train decent models directly from dataframe or excel.

### Approaches
Most of the literature that I have looked at falls into categories:
1. **Reinforcement Based**: <br>
    Where people are trying to formulate the problem of Architecture Search using Policy Gradient. They have one Controller Network (RNN) that is used to sample new architectures. And policy is learnt using the parameters of this controller network. <br>
    Problem with this approach is that it is computationally super expensive because you need to train these samples independently. 
2. **Progressive**: <br>
    This approach starts with a parent architecture and stack on layers one by one. Keeping one big gigantic network.<br>
    One variant of this approach is DART. It relaxes the discrete optimization problem into continuous space.
    These methods are less expensive to train but use lots of tips and tricks. 

### Some out of the box tools
These are some of the tools that are worth trying out before you do anything:
1. Rasa NLU
2. Ludwig
3. H<sub>2</sub>O Auto ML

### Background
Its good to know these topics if you are trying to approach this problem in the traditional RL way:
- Markov Decision Processes (MDPs)
  - Transition Matrices
  - Concept of rewards
  - What does it mean to solve an MDP? <br><sub>_It means that we need to find a policy dictating what actions to take in a particular state such that the overall reward is maximized_</sub>
- Partially Observable Markov Decision Processes (POMDPs)
  - You don't know your current state
  - Belief Space
- Hidden Markov Models (HMMs)

### Material

- Neural Architecture Search: A Survey [link](https://arxiv.org/pdf/1808.05377.pdf)
- Consider watching this great video about Neural Architecture Search [link](https://www.youtube.com/watch?v=wL-p5cjDG64)

### Publications
- 
