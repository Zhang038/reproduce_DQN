[![](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/purdue-cs-logo.jpeg)](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/purdue-cs-logo.jpeg)
# Reproduce DeepQueueNet: Towards Scalable and Generalized Network Performance Estimation with Packet-level Visibility

---

#### Group members
Yuanyuan Zhang, Jiaxin Du, Luhan Sheng, Rashmi Bhaskara, Yijiang Zhu and Zhuoyan Li


#### Motivation and Problem Statement

---

Network operators rely heavily on network simulators to successfully accomplish critical tasks such as capacity planning, topology design, and parameter tuning. Network simulators are not equipped with the capability to show packet statuses in a timely manner or provide an exact estimation of packet delay time and jitter. Therefore, it is imperative to develop a tool to realize packet-level visibility and predict the RTT per packet. This assists in addressing crucial issues like which device adds the most delay to a flow or where the bottleneck of the topology is located given a traffic pattern.

#### Our Reproduction and Results

---
DeepQueueNet[2] is such an end to end network simulator developped by deep learning, whose architecture consists of bi-LSTM as encoder and decoder and transformer to capture relatively important relationship among time series packets. Thus in our work, we reproduced DeepQueueNet with pytorch and did basic ablation experiments to study deeply about the specific encoder and decoder modules with BiLSTM, which is based on such an assumption that Bi-LSTM is redundant while transformer is also integrated into the model, so we replaced the Bi-LSTM with other modules and compare the performance.

###### Reproduction result 1

---
![](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/correlations_all.png)
###### Reproduction result 2

---
![](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/delay_analysis_train.png)
###### Reproduction result 3

---
![](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/delay_analysis_test1.png)
###### Reproduction result 4

---
![](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/delay_analysis_test_2.png)
###### Ablation study result 1

---
![](https://github.com/Zhang038/reproduce_DQN/blob/main/figures/ablation.png)

#### Conclusion
1. We successfully complete the reproduction of DeepQueueNet and validate the correctness of our work.
2. The ablation study we have conducted demonstrates that although transformer is already in the model to encode sequential information, BiLSTM also plays a fundamental role to catch time serial features about incoming packets.

#### References
- [1] [DQN source code](https://github.com/HUAWEI-Theory-Lab/deepqueuenet)
- [2] [Yang, Qingqing, Xi Peng, Li Chen, Libin Liu, Jingze Zhang, Hong Xu, Baochun Li, and Gong Zhang. "DeepQueueNet: towards scalable and generalized network performance estimation with packet-level visibility." In Proceedings of the ACM SIGCOMM 2022 Conference, pp. 441-457. 2022.](https://dl.acm.org/doi/abs/10.1145/3544216.3544248?casa_token=zRdKq6SH8NsAAAAA:it5hfhcuWwnWy5NiaWuUnmmRh_K9gM2UHWsjvvRrJQehZlo8JUqC2BGCF1wlllJAXA7WpJquW2mIiA)
  
