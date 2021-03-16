# Reinforcement learning framework

## Context
This repository has been created as part of a toy implementation of the BARBAR algorithm from the paper "Better Algorithms for Stochastic Bandits with Adversarial Corruptions" (Gupta et al., 2019) (https://arxiv.org/abs/1902.08647v2). BARBAR is a multi-armed bandits algorithm robust to corruption introduced in the rewards.

In order to compare the BARBAR performances to other standard bandits algorithms, a whole framework has been designed, consiting of three main classes: Environment, Player, Adversary.

## Setup
Environment class: defines the basic setup in which the game will take place, that is the number of arms and their reward distribution. Three distributions are proposed: Uniform, Bernoulli and Beta.

Player class: defines the strategy of the player, i.e. which action to take, and the update of the arms representation with respect to the possibly corrupted reward. The implementation includes BARBAR, UCB (Upper Confidence Bound), AAE (Active Arm Elimination) and Thompson (only implemented for the Uniform environment) algorithms.

Adversary class: defines the level of corruption introduced by the adversary in the rewards. Three adversaries are implemented here: Dummy (no corruption), Uniform (same corruption on each arm issued from a uniform distribution) and Max Current (only the maximal current drawn reward is corrupted by a constant amount).
