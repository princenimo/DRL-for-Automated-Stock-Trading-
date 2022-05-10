# Final Project for  2022 CS 394R Reinforcement Learning

## Team: Charles Nimo & Chima Ezeilo 

## Training and Evaluation
Considering the stochastic and interactive nature of the automated stock trading tasks, a financial task is modeled as a Markov Decision Process (MDP) problem. The training process involves observing stock price change, taking an action and reward's calculation to have the agent adjusting its strategy accordingly. By interacting with the environment, the trading agent will derive a trading strategy with the maximized rewards as time proceeds. Run the  `run_models.ipynb` notebook to train TRPO agent and then backtest the model to examine the performance if its trading strategy. Automated backtesting tool is preferred because it reduces the human error using the Quantopian pyfolio package.


## File Structure

- **DRL-for-Automated-Stock-Trading** # main folder
  - train # the training process will terminate once it reaches the target reward
  - test # backtest the model to evaluate performance of the trading strategy
  
- **elegant_drl_model** # collection of DRL algorithms
  - config.py  # configurations (hyper-parameter)
  - **agent.py**  # DRL algorithms
  - **net.py**  # network architectures 
  - **run.py**  # training loop
  - **env.py**  # environments for RL training

## Requirements

    Necessary:
    | Python 3.6+     |
    | PyTorch 1.6+    |

    Not necessary:
    | Numpy 1.18+     | For ReplayBuffer. Numpy will be installed along with PyTorch.
    | gym 0.17.0      | For env. Gym provides tutorial env for DRL training. (env.render() bug in gym==0.18 pyglet==1.6. Change to gym==0.17.0, pyglet==1.5)
    | pybullet 2.7+   | For env. We use PyBullet (free) as an alternative of MuJoCo (not free).
    | box2d-py 2.3.8  | For gym. Use pip install Box2D (instead of box2d-py)
    | matplotlib 3.2  | For plots.

    pip3 install gym==0.17.0 pybullet Box2D matplotli
