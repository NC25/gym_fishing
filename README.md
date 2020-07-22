# Background

The purpose of gym_fishing is to develop RL agents that can simulate fisheries. Fisheries are areas where fishes are harvested for commercial purposes. However, there is an imminent problem with how these fisheries are carried out. According to the Food and Agriculture Organization, over 33% of the world's fisheries are overfished, meaning that fish are caught and harvested more than they can reproduce (Sustainable Fisheries). Overfishing is also related to bycatch, which is the capture of unwanted sea life (WWF). Overall, this negatively affects billions of sea animals and the ecosystems they live in. It is also important to note that fisheries are a principal component for the world's food industry and economy, and overfishing is a large cause in worldwide malnourishment.

With this repository, agents will be able to simulate fisheries and determine the reproductive rates of a fishing population. It will see the necessary steps, whether to maintain the population or harvest a select percentage. This will lead to full exploitation, which yields optimum food security and an environment that is sustainable and has reached maximum potential. By comparison, over-exploitation will result in unsustainable fisheries, and under-exploitation will result in a lack of food security. After some time, we will be able to simulate more real-world environments and ecosystems for other conservation and environmental issues.

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

So far, I have used a Soft Actor Critic agent. With this algorithm, the model is able to optimize a policy while using a Q function to make training efficient but also encourages entropy (random sampling to make the model explore more). As a result, the agent will have more efficient training while having a better policy of obtaining the best reward
The library I used is Stable Baselines, a set of Reinforcement Learning algorithms for Open AI Gym.

The library I used is Stable Baselines, a set of Reinforcement Learning algorithms for Open AI Gym.

# Resources

To learn more the theory used and its application to Machine Learning, please read about Carl Boetigger's fishing baselines and [Reed's 1979](https://www.sciencedirect.com/science/article/abs/pii/0095069679900147?via%3Dihub) 'constant escapement' policy

 [WWF on Overfishing](https://www.worldwildlife.org/threats/overfishing)

[Sustainable Fisheries on Overfishing](https://sustainablefisheries-uw.org/fact-check/how-many-fisheries-are-overfished/#:~:text=Currently%2C%20the%20Food%20and%20Agriculture,exploited%20(%E2%80%9Coverfished%E2%80%9D).&text=A%20recent%20estimate%20showed%20that,18%25%20come%20from%20unsustainable%20fisheries.)
