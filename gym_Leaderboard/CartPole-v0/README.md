# CartPole-v0

- Convergence episode: 12
- max step per episode: 200
- algorithm: sac+gumbel[[code]( https://github.com/StepNeverStop/RLs/blob/master/Algorithms/tf2algos/sac.py )]
- Actor
- - 64 -> 32 -> logits
- Critic_Q
- - 64 -> 64 -> 1
- Critic_V
- - 32 -> 32 -> 1
- n_step: 4
- step_before_train(random): 10000
- agents in parrallel: 10

Parameters:
```
'auto_adaption': True,
'gamma': 0.99,
'ployak': 0.995,
'lr': 5.0e-4,
'discrete_tau': 1.0,
'max_episode': 50000,
'batch_size': 4096,
'buffer_size': 200000,
'use_priority': False,
'n_step': True
```

Result:

![](./result.gif)

![](./training_process.png)

![](./training_curve.png)
