# Project 1: Navigation

### Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.  

![Trained Agent][image1]

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in the assignment, the agent must get an average score of +13 over 100 consecutive episodes. However in the submission few improvement were made and the agent get an average score of +15 over 100 consecutive episodes

### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the course GitHub repository, in the base folder, and unzip (or decompress) the file. Ib the `Navigation.ipynb` change the cell 
    ```python
   env = UnityEnvironment(file_name="Banana_Windows_x86_64\Banana.exe")
   ```
   with the file name and folder corresponding to your operating system

### Description

*   The complete code is inside the `Navigation.ipynb` running the cells in order will 
    *   Create the environment ( do not close unitity window if it stays loading for too long as you need to run the other cells while it's open )
    *   Define the Qnetwork
    *   Define the Agent an initialise it
    *   Define dqn algoritm
    *   Train the agent
    *   Explore the result
    *   Test the model in test mode 
    *   Close the environment ( this will close the unity window )
*   The work is based on `Deep Reinforcement Learning with Double Q-learning`
*   The base implementation is based on `udacity-deep-reinforcement-learning` implementation of dqn
*   This repo contains these files :
    - `cgeckpoint.pth`: saved model weights for the Double DQN model
    - `Navigation.ipynb`: notebook containing the solution
    - `results\dddqn_new_scores.png`: score evolution during training of the model
*   To run the project the dependencies required are in the `requirements.txt` file with instructions how to create conda environment, One major difference is the Torch version as the oldest available version of torch in python 3.6 currently is 1.7.0 which is different from the recommended version.