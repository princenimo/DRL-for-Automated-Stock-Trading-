# Final Project for  2022 CS 394R Reinforcement Learning

## Team: Charles Nimo & Chima Ezeilo 

## Training and Evaluation
Considering the stochastic and interactive nature of the automated stock trading tasks, a financial task is modeled as a Markov Decision Process (MDP) problem. The training process involves observing stock price change, taking an action and reward's calculation to have the agent adjusting its strategy accordingly. By interacting with the environment, the trading agent will derive a trading strategy with the maximized rewards as time proceeds. Run the 'trpo_test.ipynb' to train TRPO agent and then backtest the model to examine the performance if its trading strategy. Automated backtesting tool is preferred because it reduces the human error using the Quantopian pyfolio package.
