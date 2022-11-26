# Reproduce the DL model with pytorch for DeepQueueNet: Towards Scalable and Generalized Network Performance Estimation with Packet-level Visibility
---

Demo paper in ACM SIGCOMM 2022


#### Abstract 
---
Network simulators are essential tools for network operators, and can assist important tasks such as capacity planning, topology design, and parameter tuning. Popular simulators are all based on discrete event simulation, and their performance does not scale with the size of modern networks. Recently, deep-learning-based techniques are introduced to solve the scalability problem, but, as we show with experiments, they have poor visibility in their simulation results, and cannot generalize to diverse scenarios. In this work, we combine scalable and generalized continuous simulation techniques with discrete event simulation to achieve high scalability, while achieving packet-level visibility. We start from a solid queueing-theoretic modelling of modern networks, and carefully identify the mathematically intractable or computationally-expensive parts, only which are then modelled using deep neural networks. Dubbed DeepQueueNet, our approach combines prior knowledge of networks, and can support arbitrary topology and device traffic management mechanisms (given sufficient training data). Our extensive experiments have shown that DeepQueueNet can achieve near-linear speed-up with the number of GPUs, and its accuracy of performance estimation is above 97.9% for average round-trip time (RTT) and 93.7% for 99th percentile RTT in all scenarios.

## Install
---
First of all, please make sure that you have at least 1 GPU on hand (16GB memory is required to run the device model). To install the right dependencies, run the following to create an environment from the `env.yml` file:
```python
conda env create -f env.yml
```
It will create a new evnvironment named `dqn_env_py36`. To activate the new environment: 
```python
conda activate dqn_env_py36 
```
## References

- [1] [DQN source code](https://github.com/HUAWEI-Theory-Lab/deepqueuenet)
- [2] [Yang, Qingqing, Xi Peng, Li Chen, Libin Liu, Jingze Zhang, Hong Xu, Baochun Li, and Gong Zhang. "DeepQueueNet: towards scalable and generalized network performance estimation with packet-level visibility." In Proceedings of the ACM SIGCOMM 2022 Conference, pp. 441-457. 2022.](https://dl.acm.org/doi/abs/10.1145/3544216.3544248?casa_token=zRdKq6SH8NsAAAAA:it5hfhcuWwnWy5NiaWuUnmmRh_K9gM2UHWsjvvRrJQehZlo8JUqC2BGCF1wlllJAXA7WpJquW2mIiA)
