# Reinforcement-Learning-with-Stable-Baselines3
This project demonstrates training and testing various reinforcement learning algorithms on Gymnasium environments using Stable Baselines3. Following concepts learned from [Johnny Code's YouTube tutorial series]

## Features

- **Flexible Training Pipeline**: Train any Stable Baselines3 algorithm (A2C, DDPG, DQN, PPO, SAC, TD3) on any Gymnasium environment
- **Smart Training Stopping**: Implements two callback mechanisms:
  - Stops when reward threshold is reached
  - Stops when no improvement is detected after specified evaluations
- **Model Evaluation**: Automatic evaluation during training with best model saving
- **TensorBoard Integration**: Training metrics logged for visualization
- **Easy Testing**: Load and visualize trained models in test mode

## Requirements

- Python 3.7+
- Gymnasium
- Stable Baselines3

## Acknowledgments

This implementation builds upon concepts taught in Johnny Code's excellent Stable Baselines3 tutorial series. Special thanks for the clear explanations on:
- Setting up evaluation callbacks
- Implementing early stopping conditions
- Proper model saving and loading techniques
- Effective TensorBoard integration

## Usage
Training

python main.py [GYM_ENVIRONMENT] [ALGORITHM]

Testing

python main.py [GYM_ENVIRONMENT] [ALGORITHM] --test

## Arguments
gymenv: Gymnasium environment name (e.g., "Pendulum-v1", "Humanoid-v4")

sb3_algo: Stable Baselines3 algorithm (A2C, DDPG, DQN, PPO, SAC, TD3)

--test: Flag to enable test mode (visualization)

## Training Details
The training process includes:

Model evaluation every 10,000 timesteps

Automatic stopping when reaching reward threshold (300 by default)

Early stopping if no improvement for 5 evaluation periods (after minimum 10,000 evaluations)

Best model saved automatically in models/ directory

Training logs saved in logs/ for TensorBoard visualization

## File Structure
.
├── models/                 # Saved models

├── logs/                   # Training logs

├── main.py                 # Main training/testing script

├── README.md               # This file

## Customization
You can modify:

Reward threshold in StopTrainingOnRewardThreshold

Evaluation frequency in EvalCallback

Early stopping parameters in StopTrainingOnNoModelImprovement

## Results
Include sample training curves or test performance metrics here for your specific experiments.







