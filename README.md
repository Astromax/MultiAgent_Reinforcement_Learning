# MultiAgent_Reinforcement_Learning

This repo contains a solution to the Unity "Tennis" environment using multi-agent DDPG.  

# Environment
In this environment, two agents each control a racket to bat a ball back & forth across a net.  The rewards are +0.1 for getting it over the net and -0.01 for letting it hit the ground or go out of bounds. 

Each agent only sees part of the environment, receiving a 24 element state vector describing the position & velocity of the ball.  Each agent's actions are two-dimensional & continuous, corresponding to moving towards or away from the net and jumping.

The environment is considered "solved" if the 100-episode average score is greater than 0.5, where the score in each episode is the larger of the scores of the two agents.  This problem is both cooperative & competitive because, although each agent wants to get the higher score, allowing the ball to go out-of-bounds ends the episode, so they must cooperate to prevent that from happening.

# Requirements & Installation
This part has been taken from a former Udacity DRL ND student (https://github.com/p-o-lo/maddpg-tennis/blob/main/README.md) because it's exactly the same & there's no need to reinvent the wheel.
To run the notebook **Tennis.ipynb** it firstly needs to set up the environment as follows:

- Create (and activate) a new kernel with Python 3.6
    - **Linux** or **Mac**
   ```
   conda create --name drlnd python=3.6
   source activate drlnd
    ```  
    - **Windows**
   ```
    conda create --name drlnd python=3.6
    activate drlnd
   ```

- If you didn't before, you need a minimal install of OpenAI gym
```
pip install gym
pip install gym[classic_control]
pip install gym[box2d]
```

- Clone the repository, and navigate to the python/ folder. Then, install several dependencies.
```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

- Create an IPython kernel for the dqn environment.
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

- Download the Unity Environment which matches your operating system
    - [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
    - [Mac](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
    - [Windows (32bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
    - [Windows (64bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

and unzip in a folder of your choice

- Then you can finally open the **Tennis.ipynb**. Before running code in this notebook
    - change the kernel to match the drlnd environment by using the drop-down Kernel menu
    
    ![This is an image](https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png)
 
    - In the following line
    ```
    env = UnityEnvironment(file_name="...")
    ```
    change the folder path where you installed the Tennis Unity environment.
