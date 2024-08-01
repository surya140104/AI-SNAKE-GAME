# AI-SNAKE-GAME
AI Snake Game created using Reinforcement Learning
   
  
  
  
Reinforcement Learning Project Report  
  
Project Title:   
Implementing Reinforcement Learning model on Snake Game  
  
  
  
  
  
  
  
  
  
  
  Team Members  
Sl. No.  	Name  	Roll Number  
1  	Surya  	CS21B1037  
2  	Vikyath  	CS21B1045  
3  	Krishna Sahit  	CS21B1048  
4                	Srishanth Reddy  	CS20B1052  
   5 	Girish 	CS21B1005  
  	  	  
  	  	  
  	  	  
  	  	  
  	  	  
RL Project Road Map  
  
Problem Statement  
Create an RL system for Snake: state includes snake position, food, and obstacles; actions cover movement directions; reward system for food consumption and collision avoidance; use Q-learning or DQN; balance exploration and exploitation; evaluate with score and length metrics; and strive for robust, high-performance gameplay.
 Introduction   
Not more than 100-word description of the problem statement.  
Pointwise description (if more details needed for introduction to the problem) Note: Survey and other details are not expected  
The aim of this project is to explore the application of reinforcement learning (RL) techniques in solving the classic Snake game. Snake, a well-known arcade game, presents a challenging environment where a player controls a snake to consume food items while avoiding collisions with obstacles and itself. By leveraging RL algorithms, we seek to develop an intelligent agent capable of autonomously learning optimal strategies for navigating the snake through the grid. This report outlines our approach, methodologies, challenges encountered, and insights gained throughout the development process. Through this project, we aim to gain a deeper understanding of RL algorithms and their practical applications in solving complex gaming scenarios.  
  
Approach  
1.	State  	  	: Represent game state with grid.  
2.	Actions   	: Specify movements – up, down, left, right.  
3.	Rewards  	: Assign positive for eating, negative for collisions.  
4.	Algorithm  	: Opted for Deep Q Learning.  
5.	Training  	: Gather experiences, train neural network.  
6.	Evaluation  	: Assess performance, adjust hyper parameters.  
7.	Environment  	: Establish game layout using a grid, including snake, food, and boundaries.  
  
  
  
   
  
Overall Working Diagram  
  
  
  
   
  
  
  
  
  
  
  


Design Details  
Environment  	: Grid-Based Snake game with border, and some food (Fruits) on the map along with  
  	  	   the agent (Snake)  
States   	: There are 11 states which are being used  
   	  	  [Danger Straight, Danger Right, Danger Left,   
  Direction Left, Direction Right, Direction up, Direction Down,   
  Food Left, Food Right, Food Up, Food Down]  
Reward    	: Eat Food - “+10”  
    	  	  Game Over- “-10” (Snake on)  
  Else - “0”  
Actions   	: [1,0,0] -> Straight  
  [0,1,0] -> Right Turn  
  [0,0,1] -> Left Turn  
Justification for Approach :  	  
Reinforcement learning allows gradual strategy improvement through trial and error. Deep Q Learning manages high-dimensional game states effectively. Neural networks aid generalization across actions and scenarios. Techniques like experience replay and reward shaping enhance learning and performance.  
Deep Q-Learning is a type of reinforcement learning algorithm that uses a deep neural network to approximate the Q-function, which is used to determine the optimal action to take in each state.  
  
  









Work Done and Results  
The Reinforcement Learning Snake Game Graph: 
 
  
The graph we describe represents a fascinating process where a machine learning model is trained to play Snake using reinforcement learning.  
 
1.	Reinforcement Learning Setup: 
In reinforcement learning, an agent (the machine learning model) learns by interacting with an environment (the Snake game) and receiving rewards for desired behaviors. In the case of Snake, the reward is likely moving the snake and collecting food, while avoiding hitting the wall or itself. 
Agent: The machine learning model acts as the agent, controlling the snake's movement. 
Environment: The Snake game environment provides the agent with sensory information (game state) and rewards/penalties for its actions. 
Rewards: The agent receives a positive reward for collecting food (growing the snake) and a negative reward for hitting a wall or itself (ending the game). 
Action Space: The agent can choose from a set of actions like moving Up, Down, Left, or Right. 
 
 
2.	Information in the Graph: 
 
X-axis: Represents the number of games played by the agent. This signifies training progress. 
Y-axis: Represents the score achieved in each game. This could be the length of the snake at the end or points accumulated. 
Data Points: Each point on the graph signifies the outcome of a single game. As training progresses, the points should ideally show an upward trend, indicating the agent's learning. 
Trendline: The line superimposed on the data points (if present) is a statistical model trying to capture the relationship between the number of games played (x) and the score achieved (y). 
 
 
3.	Training Process: 
 
Initially, the agent's actions might be random, leading to low scores. 
With each game, the agent receives feedback (rewards) and updates its internal model (neural network) to choose better actions in the future. 
Over many games, the agent learns to prioritize actions that maximize rewards and achieve higher scores. 
The upward trend in the graph reflects this learning process. 
 
 
4.	Factors effecting: 
 
The specific reinforcement learning algorithm used (e.g., Q-Learning) would influence how the agent learns from rewards and updates its policy. 
Hyperparameters like learning rate and exploration rate affect the speed and efficiency of learning. Visualizing the snake's movement along with the graph can be helpful to understand the agent's strategies and learning process. 
This reinforcement learning Snake game experiment showcases how an agent can learn complex behaviors through trial and error, making it a valuable tool for training AI in various domains. 
 
 
5.	Output Interpretation: 
 
"Game 498 corresponds to a score of 30": This indicates that in the 498th game, the agent achieved a score of 30. 
"x=56.97 y=1.800": This equation might represent the trendline, where x is the number of games played and y is the predicted score based on the model. Score:9. 
 
 
 
 
  
 
 
 
 
 
The graph we describe showcases the application of reinforcement learning (RL) to train an AI agent to play the classic game Snake.  
 
1.Information in the Graph: 
 
X-Axis: Episodes (Games Played) 
 
This axis represents the number of complete games (episodes) the AI agent has participated in during training. Each episode is a fresh start where the snake begins at a specific position and aims to consume food items without hitting walls or its own body. 
The limited range of 0 to 12 episodes suggests this might be a preliminary experiment or an excerpt from a longer training process. 
Y-Axis: Reward (Performance Score) 
 
This axis measures the agent's performance during an episode, typically indicated by a reward score. A higher score (closer to 1) signifies better performance. In Snake, the reward could be directly related to the snake's length (longer is better) or a combination of factors like length, number of food items eaten, and avoiding collisions. 
The graph doesn't depict negative rewards (penalties) for bad actions, but they're likely part of the training process. Hitting walls or its own body would likely result in a negative reward. 
 
Points: Each data point on the graph represents the agent’s score after a certain number of games played. For instance, the point at x = 4, y = 0.2 represents the agent’s score of 0.2 after playing 4 games. 
 
2.Interpreting the Output: 
 
"Game 10 Score 1 Record: 1": This indicates that in the 10th game, the agent achieved a score of 1. Additionally, "Record: 1" might signify this is the highest score achieved so far during training. 
Score:0 
0.1535 will represent the average reward the AI agent received after playing 4 games (shown by a data point at x = 4 on the graph). 
 
In the context of the graph about AI playing Snake using reinforcement learning, a higher reward signifies better performance. So, a score of 0.1535 after 4 games suggests the agent's performance is still in the early stages of learning. 
 
