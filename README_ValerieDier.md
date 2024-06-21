# Reinforcement Learning Introduction - PuddleWorld  

## Motivation  

This project is an introductory effort to train an agent in the PuddleWorld environment using basic reinforcement learning (RL) algorithms.  The work was proposed by AMII (Alberta
Machine Intelligence Institute) as part of a friendly competition and learning opportunity in the lead-up to their Upper Bound AI conference in late May 2024.  The main objective 
is to become familiar with RL terminology, the main ways RL problems are tackled, the advantages and pitfalls of using RL, and where RL approaches may be applied.  Relevant 
libraries are also discovered, and an attempt to optimize hyperparameters is made using optuna.  

Ultimately, a DQN agent was trained with limited success: some episodes completed to the goal (successful termination) while many others times out (on maximum time steps).  
Consistent performance was not achieved in time for the conference in order to be able to submit results.  Attempts to use optuna to tune hyperparameters did not throw errors, but
they also did not result in a completed study.  The effort may have to migrate to another platform to reach successful conclusion.

## Note on files/repository  

The files in this repository primarily came from cloning AMII's repository for this competition.  Modifications to any notebooks, etc, were to be pushed to my own repo (this one). 
Many of the files found here are therefore not my creations.  I have so far created getting_started_development.ipynb, predictably, from getting_started.ipynb, which was kindly 
provided by AMII.  Files from other folders are required to run the code, such as environment configuration files, so it was simplest to keep the entire repo and add to the 
files once they resided on my own repo.  

The intention is to clean up the notebook files once a few approaches have shown some success.  The "...development" notebook is a first pass at basic RL libraries and methods.

## General Approach   

Some amendments were made to the AMII-provided notebook to get around some errors that were occurring for the local set-up.  These are documented in the notebook.  After running the 
random and human agents without errors, efforts began on a DQN agent.  An initial attempt at hyperparameter tuning using optuna indicated that it might be best to reduce the number of 
hyperparameters to iterate on - this would reduce the computational effort required by eliminating a good number of combinations to trial.  

## Results  

The DQN agent yielded inconsistent results, likely due to the hyperparameters set.

## Challenges  

Challenges were encountered at various points in this project:

1.  Errors were initially encountered trying to run the default notebook mainly due to differences in platform used.  Visualization of results in particular proved time-consuming 
to address.  

2.  DQN agents allow for the configuration of many hyperparameters, with no clear idea of the ranges that might best work for a given environment and its rewards scheme.  Sometimes
a successful termination was reached, but many times it wasn't even as time steps were greatly increased.  Learning rate seemed reasonably impactful, but results were difficult to 
reproduce.

3.  Using optuna to trial several combinations of hyperparameters proved too intensive for the local set-up used.  A future study set-up on a cloud platform (google colab, etc) may 
prove more helpful.

## Development Work   

Generally two objectives are identified:  

1.  Gain a better understanding of how an RL problem can be set-up and how the different architectures, like DQN, or DPO, etc, operate.  

2.  Learn more about tuning RL agent architectures for more targeted approaches to reaching succesful training.

## Acknowledgements   

I wish to acknowledge the assistance of the organizers at AMII (Alberta Machine Intelligence Institute) and participants.  

## Revision History  

**June 20 2024**  
Document updated to reflect where the work was left and where future efforts might pick up.  
  