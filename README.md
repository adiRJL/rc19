# Reinforcement Learning for Recommendation Systems

## Abstract

The project focuses on developing a novel approach for recommendation systems using Reinforcement Learning (RL). Traditional recommender systems often treat recommendations as static, assuming users' preferences remain unchanged. RL addresses this by considering recommendation as a sequential decision-making process, optimizing for cumulative feedback over time. The proposed framework utilizes a Deep Q-Network (DQN) based on the Double Q-Network model, employing two networks - Policy and Target, to model the user's state as a sequence of movies watched.

## Proposed Approach

### 1. Modelling the MDP
- The user's state is modeled as a sequence of the last four movies watched.
- Recommender process treated as a Markov Decision Process (MDP).
- Action space includes all movies for recommendation.
- Q-function used to evaluate the goodness of each state-action pair.

### 2. Dataset
- MovieLens 1M dataset chosen for structured user and movie information.
- 10% of the dataset initially used, containing 6040 unique users and 3700 movies.

### 3. Framework Architecture
- User's state represented by a 1200-dimensional vector based on a sliding window of four movies.
- DQN architecture with a neural network trained over thousands of episodes.
- Experience Replay employed to avoid estimation bias.
- Policy Network and Target Network used to bridge the gap between predicted and target Q-values.

## Results

Precision was employed as a metric, considering the relevance of recommended movies based on user feedback. Test results over multiple trials showed precision values ranging from 0.62 to 0.68.
