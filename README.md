# Candy
Candy: Self-driving in Carla Environment.

 ![image](https://github.com/createamind/candy/blob/master/screenshots/candy.png)

What is candy? A model with the structure: Hierarchical Observation -- Plan&Policy -- Hierarchical Actions

## Running Candy
(This project is still working in progress.)
* Download Carla-0.8.2 from [here][carlarelease].
* Start CarlaUE4 engine in server mode, using commands from [here][carlagithub].
* Run `python main.py -m Town01 -l` (Specifying town number and enable lidar).

[carlagithub]: http://carla.readthedocs.io/en/latest/running_simulator_standalone/
[carlarelease]: https://github.com/carla-simulator/carla/releases


## Candy Features
* Use C3D for observation abstraction.
* Combining imitation learning and reinforcement learning.
* Use MCTS for planning.
* Plenty of auxiliary tasks for robust hidden representation.
* Persistent training process and flexible architecture.

## Todo
* Change Policy Gradient to PPO(Proximal Policy Optimization).
* Solve the failure of policy training.
* Implement MCTS.
* Visualize parameter transition.
* Policy embedding? Curiosity, Attention, Memory ?
* Prioritied Replay
* Distributed


## Code Components
* main.py: Main file. It Deals with Carla environment.
* carla_wrapper.py: Wrap main.py, buffer information for the model.
* persistence.py: Main model file. It is for building the big graph of the model.
* modules/* : Building blocks of the model, used in persistence.py.


