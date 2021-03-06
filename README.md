# LastOrder
LastOrder is a StarCraft AI bot developed by Bilibili AI Lab.  
LastOrder uses a pre-trained model to do macro action selection during game. The model combines APE-X DQN with LSTM and is trained distributively on cluster.  

The detailed info can be found in:  
[Macro action selection with deep reinforcement learning in StarCraft](https://arxiv.org/abs/1812.00336)

## Installation
LastOrder comprises of two parts:
* Actor. running the StarCraft client and processing messages with model. 
  * In training mode, actor periodically receive updated model from learner. 
  * In evaluation mode, actor load the local pre-trained model and run independently without learner.
* Learner. running the training procedure and updating model to actors.

### Actor Requirements
* BWAPI 4.2.0.
* VisualStudio 2017 supplied with the Development Tools for C++.
* Python 3.6 with tensorflow and zmq 

### Actor Installation
* Setting the env variables: `BWAPI_DIR`, pointing to BWAPI 4.2.0 installation.
* Copy the libzmq_LastOrder.dll into C:\Windows
* Copy pre-trained model data to AI\saved_model

### Learner Requirements
* Python 3.6 with tensorflow and zmq
* [StarcraftAITournamentManager](https://github.com/davechurchill/StarcraftAITournamentManager)



