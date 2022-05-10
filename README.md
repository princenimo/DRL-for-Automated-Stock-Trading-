# Final Project for  2022 CS 394R Reinforcement Learning

## Team: Charles Nimo & Chima Ezeilo 

## Training and Evaluation
Considering the stochastic and interactive nature of the automated stock trading tasks, a financial task is modeled as a Markov Decision Process (MDP) problem. The training process involves observing stock price change, taking an action and reward's calculation to have the agent adjusting its strategy accordingly. By interacting with the environment, the trading agent will derive a trading strategy with the maximized rewards as time proceeds. Run the  `trpo_test.ipynb` notebook to train TRPO agent and then backtest the model to examine the performance if its trading strategy. Automated backtesting tool is preferred because it reduces the human error using the Quantopian pyfolio package.


## File Structure

- **DRL-for-Automated-Stock-Trading** # main folder
  - train # a collection of training programs

  	- config.py  # configurations (hyper-parameter)
  	- **run.py**  # training loop
  	- worker.py  # the worker class (explores the env, saving the data to replay buffer)
  	- learner.py  # the learner class (update the networks, using the data in replay buffer)
  	- evaluator.py  # the evaluator class (evaluate the cumulative returns of policy network)
  	- replay_buffer.py # the buffer class (save sequences of transitions for training)
- **elegant_drl_model** # collection of DRL algorithms
  - config.py  # configurations (hyper-parameter)
  - **agent.py**  # DRL algorithms
  - **net.py**  # network architectures 
  - **run.py**  # training loop
  - **env.py**  # environments for RL training
