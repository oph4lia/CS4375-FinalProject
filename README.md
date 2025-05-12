# CS4375.501 Final Project Brainstorming
> Mikkael Dumancas

## Proposals

There are 3 options for this project
1. Classification on structured datasets
2. NLP and text classification
3. Option of your choice

Given these options, I went with option 3. The premise of my project is building a **Reinforcement Learning Agent** to play the google chrome web game, Dino Run (also known as the "no internet" game).

## Understanding Reinforecement Learning

Here is a simple explanation taken from the documentation of [*Gymnasium*](https://gymnasium.farama.org/introduction/basic_usage/), an OpenAI API built to support single agent reinforcement learning environments:

> "The agent receives an observation about the environment, the agent then selects an action, which the environment uses to determine the reward and the next observation. The cycle then repeats itself until the environment ends (terminates)."

Simply put, reinforcement learning is a simple approach to ML that involves the core concept of a reward. An RL model (or agent) seeks to maximize this reward signal via continuous decisions made on observations.

# Notes

- Determining when game is over: Embedded Machine Learning (Vectorized image)
- RL at a high level is:
  - Model interacts with an external system known as an *environment*
  - Model makes observations of the environment
    - With each observation, model makes an action based on policies and receives a reward from environment
    - The environment also gives an update of the state of the env to the model and confirms if the episode is not terminated
    - If not terminated, model updates Q-value and makes next decisive action
  - Each iteration is added to the observed trajectory (one iteration is called a rollout)

Preprocessing techniques

- State/Observation preprocessing
  - Normalizing state variable ranges (-1,1 or 0,1) to improve learning stability and convergence
  - Transform features to have zero mean and unit variance
  - Image processing, including grayscaling, resizing, frame stacking (temporal information), edge detection or other feature extractions
  - Reward preprocessing
    - Scale rewards to a normalized range
    - Clip/limit rewards to prevent instability
    - Apply temporal discount factors to prioritize immediate rewards (Bellman's)
  - Feature preprocessing
    - Select/construct relevant features from raw observations
    - Extract features using techniques like principal compopnent analysis to reduce dimensionality
  - Experience buffer preprocessing
    - Prioritize experience replay to focus on important transitions
    - Normalize batches of experiences
    - Relabel reperiences with different goals to increase learning efficiency
> Need to research preprocessing techniques







