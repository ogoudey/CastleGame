## CastleGame
This is the environment for a class project.

### Requirements
- Linux, python

### Installation
1. Clone the repo.
2. Clone the [agent architecture](https://github.com/ogoudey/VLA_Star)
3. Link the agent to Unity with:
```
ln /path/to/VLA_Star/experiments/unity_robot_run.sh /path/to/CastleGame_Data/Scripts/
```
4. Assign the VLA_STAR_PATH environment variable to /path/to/VLA_Star
4. Put OPENAI_API_KEY in your `.bashrc` or elsewhere.

### Gameplay
The goal is to get to the ATM machine at the center of the castle.

#### Controls
- `WASD` to move, `mouse` to look around, `Space` to jump, and `E` to interact.

#### The map
1. There are two gates which are each opened when someone (or _something_) steps on a corresponding pressure plate.
2. Behind each gate (and to the right), there is a lever that someone (or something) can switch to keep the gate opened or closed.

#### The agent
The agent can be activated with `E`. Then, you can chat with it. It knows about the things in the world, but has no goal other than to help you.

The agent can be configured by editting the architecture code:
```
unity_robot_run.sh > unity_robot_phase.py > shop.instantiate_unity_robot() > ...
```
