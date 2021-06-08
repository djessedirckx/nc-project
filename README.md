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
jupyterlab==2.2.6
numpy==1.19.2
opencv-python==4.5.1.48
pandas==1.1.3
scikit-image=0.17.2
scikit-learn
tensorflow==2.4.1
```

For running the Atari environment, a ROM file containing the game dynamics is required. This can be found [here](http://www.atarimania.com/rom_collection_archive_atari_2600_roms.html).

## Files

The files in this repository are distributed over multiple folders
- Images:
  - [Results of the Genetic Algorithm implementation](images/GA)
  - [Results of the CMA-ES algorithm](images/CMA-ES)
- RNN weights
  - [Weights for RNN trained on an action space of 4](rnn%20weights/rnn_predictor_4_actions.hdf5)
  - [Weights for RNN trained on an action space of 9](rnn%20weights/rnn_predictor_9_actions.hdf5)
- Source code:
  - [Data collection for VAE](source%20code/VAE_data_collection.ipynb)
  - VAE implementation
  - [RNN implementation and testing](source%20code/RNN_implementation.ipynb)
  - Random agent used to establish baseline results
  - Implementation and testing of the SQM algorithm
  - Implementation and testing of the genetic algorithm
  - CMA-ES
    - [State-only experiments](source%20code/CMAES_9_actions.ipynb)
    - [RNN experiment](source%20code/CMAES_9_actions_rnn.ipynb)