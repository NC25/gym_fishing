# Background

The purpose of gym_fishing is to develop RL agents that can simulate fisheries. Fisheries are areas where fishes are harvested for commercial years. However, there is an imminent problem with how these fisheries are carried out. According to the Food and Agriculture Organization, over 33% of the world's fisheries are overfished, meaning that fish are caught and harvested more than they can reproduce. Overfishing is also related to bycatch, which is the capture of unwanted sea life (WWF). Overall, this negatively affects billions of sea animals and the ecosystems they live in. It is also important to note that fisheries are a principal component for the world's food industry and economy, and overfishing is a large cause in worldwide malnourishment.

# Setup
For Python setup, install the following dependencies:
```
python gym_fishing/setup.py sdist bdist_wheel 
pip install -e ./gym_fishing/
```
```
ls
cd gym_fishing
```

# Environments 
 
A continuous state space of fish biomass, with:
* Discrete action space with three actions: maintain harvest level, increase harvest by 20%, decrease harvest by 20%
* Discrete action space with n > 3 actions: action is taken as quota, quota = action / n_actions * K
* Continuous action space, action = quota. 
(Boettiger)

# Interface
So far, I have used a Soft Actor Critic agent. With this algortihim, the model is able to optimize a policy while using a Q function to make training effecient but also encourages entropy (random sampling to make the model explore more). As a result, the agent will have more effecient training while having a better policy of obtaining the best reward

The library I used is Stable Baselines, a set of Reinforcement Learning algorithims for Open AI Gym.

# Resources

To learn more the theory used and its application to Machine Learning, please read about Carl Boetigger's fishing baselines and * [Reed's 1979](https://www.sciencedirect.com/science/article/abs/pii/0095069679900147?via%3Dihub) 'constant escapement' policy
