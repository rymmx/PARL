## Reproduce PPO with PARL
Based on PARL, the PPO model of deep reinforcement learning is reproduced, and the same level of indicators of the paper is reproduced in the classic Mujoco game.
Include following approach:
+ Clipped Surrogate Objective
+ Adaptive KL Penalty Coefficient

> PPO in
[Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347)

### Mujoco games introduction
Please see [here](https://github.com/openai/mujoco-py) to know more about Mujoco game.

### Benchmark result

<img src=".benchmark/PPO_HalfCheetah-v2.png" width = "400" height ="300" alt="PPO_HalfCheetah-v2" />  

## How to use
### Dependencies:
+ python3.5+
+ [paddlepaddle>=1.0.0](https://github.com/PaddlePaddle/Paddle)
+ [parl](https://github.com/PaddlePaddle/PARL)
+ gym
+ tqdm
+ mujoco-py>=1.50.1.0

### Start Training:
```
# To train an agent for HalfCheetah-v2 game (default: CLIP loss)
python train.py

# To train for different game and different loss type
# python train.py --env [ENV_NAME] --loss_type [CLIP|KLPEN]
