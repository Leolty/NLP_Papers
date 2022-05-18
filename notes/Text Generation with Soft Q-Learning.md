# Text Generation with Soft Q-Learning

## 1. url and bibtex

https://arxiv.org/abs/2106.07704

```bibtex
@article{2021Text,
  title={Text Generation with Efficient (Soft) Q-Learning},
  author={ Guo, H.  and  Tan, B.  and  Liu, Z.  and  Xing, E. P.  and  Hu, Z. },
  year={2021},
}
```



## 2. Challenges of text generation for RL
- sparse reward ( agent receives non-zero award only after the full sequence is generated )
- large action space (millions of vocabularies)

##3.  Two major RL approaches
1. Policy-based RL  ( Policy Gradient)
  most samples are with 0 reward
2. Value-based RL (Q-Learning)
  unstable and inefficient

## 4. Soft Q-Learning

Haarnoja, Tuomas, et al. “Reinforcement Learning with Deep Energy-Based Policies.” ICML’17 Proceedings of the 34th International Conference on Machine Learning - Volume 70, 2017, pp. 1352–1361.

### Traditional Q-Learning:

- Q-learning defines a *Q(s,a)* function, which refers to the expected value of the cumulative reward obtained after taking action *a* in state *s*.

- Limitations:

  Because Q-learning uses the action corresponding to the optimal value at the next moment when updating the Q function, this will lead to an "excessive" estimate of the sampled action



### SQL's key

- Ensure that the agent is able to both prioritize the most promising actions and consider other actions
- (Iterate over the soft Bellman equation to let the Q value converge.)
- (the agent is encouraged to optimize the reward while staying as stochastic as possible)



##5. PCL

 updates Q-values of all tokens at once through a connection between the value function and the induced policy. 
- Multi-step PCL: resolve the potential instability issue due to the bootstrapped V value and the sparse reward 

- joint on-policy and off-policy training: first train model with on-policy for warming up, joint on- and off- policy training to maximum the reward

  ​

## 6. Conclusion

 develop a new RL formulation for text generation based on SQL and PCL