# Natural computing project: World model for MsPacMan
## Students 
- Lieuwe Meijdam (s1047496)
- Marius M. Kästingschäfer (s3058301)
- Djesse Dirckx (s1046968)

## About
This repository contains all software that was used for the final project of the Natural Computing () course. In this project, it was tried to implement the World Model architecture for the game MsPacMan(). Specifically, it was evaluated which approach (genetic algorithm vs. evolutionary strategy) works best for optimising the parameters of the controller component. The following sections describe requirements and files that are needed to replicate results.

## Requirements
All code in this repository is written in the Python programming language. To be able to succesfully run the experiments, the following dependencies are required:
```python
atari-py==0.2.9
cma==3.0.3
gym==0.18.3
h5py==2.10.0
notebook==6.1.4
matplotlib==3.3.2
numpy==1.19.2
opencv-python==4.5.1.48
pandas==1.1.3
scikit-image=0.17.2
scikit-learn==0.23.2
tensorflow==2.4.1
```

For running the Atari environment, a ROM file containing the game dynamics is required. This can be found [here](http://www.atarimania.com/rom_collection_archive_atari_2600_roms.html). 

## Usage

### VAE & RNN
The steps below can be followed for replicating the VAE and RNN experiments:
- The data required for training the VAE can be generated using the [Data collection for VAE](source%20code/VAE_data_collection.ipynb) notebook.
- To use the RNN, either the listed pretrained models or the [notebook for training the RNN](source%20code/RNN_implementation.ipynb) can be used for retraining the model.

### Controller experiments
In order to repeat the various experiments to find an optimal strategy for the agent, the respective notebooks listed under `Files` can be used. It is important to execute these notebooks from top to bottom in order to get proper results. All experiments can be conducted independent from each other. Each notebooks contains detailed comments about its components.

## Files
The files in this repository are distributed over multiple folders
- Images:
  - [Results of the SQM algorithm](images/SQM)
  - [Results of the Genetic Algorithm](images/GA)
  - [Results of the CMA-ES algorithm](images/CMA-ES)
- RNN weights
  - [Exported RNN trained on an action space of 4](rnn%20weights/rnn_predictor_4_actions.hdf5)
  - [Exported RNN trained on an action space of 9](rnn%20weights/rnn_predictor_9_actions.hdf5)
- Source code:
  - [Data collection for VAE](source%20code/VAE_data_collection.ipynb)
  - [VAE implementation](source%20code/VAE.ipynb)
  - [RNN implementation and testing](source%20code/RNN_implementation.ipynb)
  - [Implementation and testing of the SQM algorithm](source%20code/Sequence-Mutation.ipynb)
  - [Implementation and testing of the genetic algorithm](source%20code/Genetic-Algorithm.ipynb)
  - CMA-ES
    - [Gamestate-only experiments](source%20code/CMAES.ipynb)
    - [Gamestate + RNN experiment](source%20code/CMAES_RNN.ipynb)

## Videos
- SQM
  - [Best configuration for action space 4 (game state as input only)](https://youtu.be/dtlEn2XuvG0)
  - [Best configuration for action space 9 (game state as input only)](https://youtu.be/jjMcVD5XEzw)
- GA
  - [Best configuration for action space 4 (game state as input only)](https://youtu.be/cLe5OKIZM9k)
  - [Best configuration for action space 9 (game state as input only)](https://youtu.be/263EwEyo18g)
  - [Best configuration for action space 9 (game state and RNN hidden state as input)](https://youtu.be/BTYWLt3w4Rk)
- CMA-ES
  - [Best configuration for action space 4 (game state as input only)](https://www.youtube.com/watch?v=HclX0dUzcFk)
  - [Best configuration for action space 9 (game state as input only)](https://www.youtube.com/watch?v=pDvYLiPEWgg)
  - [Best configuration for action space 9 (game state and RNN hidden state as input)](https://www.youtube.com/watch?v=WevmIJDQK5s)

