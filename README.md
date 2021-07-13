[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135605-ba0e5f2c-7d12-11e8-9578-86d74e0976f8.gif "Trained Agent"

# MountainCar-V0

### Instructions

How to discretize continuous state spaces, to use tabular solution methods to solve complex tasks.

## Environment

![Trained Agent][image1]

### Goal
Get an under powered car to the top of the hill (top = 0.5 position)

### State-Space

Type: Box(2)

|  Observation  | Min  | Max |
|     :---:     |----- | ----|
|   `position`  | -1.2 | 0.6 |
|   `velocity`  | -0.07| 0.07|

### Action-Space

Type: Discrete(3)

| Num   | Action  |
| :---: | ------  |
|  0  | push left |
|  1  | no push |
|  2  | push right |


### Reward
-1 for each time step, until the goal position of 0.5 is reached. As with MountainCarContinuous v0, there is no penalty for climbing the left hill, which upon reached acts as a wall.

### Results

MountinCar-v0 defines "solving" as getting average reward of -110.0 over 100 consective trails


### Resources

To learn about more advanced discretization approaches, refer to the following:

- Uther, W., and Veloso, M., 1998. [Tree Based Discretization for Continuous State Space Reinforcement Learning](http://www.cs.cmu.edu/~mmv/papers/will-aaai98.pdf). In _Proceedings of AAAI, 1998_, pp. 769-774.
- Munos, R. and Moore, A., 2002. [Variable Resolution Discretization in Optimal Control](https://link.springer.com/content/pdf/10.1023%2FA%3A1017992615625.pdf). In _Machine Learning_, 49(2), pp. 291-323.
