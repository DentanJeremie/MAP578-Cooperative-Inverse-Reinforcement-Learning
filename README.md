# Cooperative Inverse Reinforcement Learning - Simulations

## Jérémie Dentan, Philippe Nugnes, Nathanaël Cuvelle--Magar

### Context

This notebook is part of a work on the following paper : *Cooperative Inverse Reinforcement Learning*, Dylan Hadfield-Menell, Anca Dragan, Pieter Abbeel, Stuart Russell, 2016 (https://arxiv.org/abs/1606.03137), which is also available on this Github repository, with its supplementary.

Our work is part of a project for the course "MAP578 - Emerging topics in artificial intelligence" of École Polytechnique, France, taught by Aymeric Dieuleveut and El Mahdi El Mhamdi.

### Our work

We had several objectives for this projects :
   * Formalizing the reduction between CIRL and POMDP and DEC-POMDP. This reduction is discussed in the slides available on the repository.
   * Simulating a CIRL and showing how an approximation of the optimal teaching strategy in a CIRL game can overperform Demonstration By Expert.

### Simulations
The context of this simulation is the following. It is an adaptation of the proof of theorem 3 in the paper's supplementary.
   * Let consider two population during an election : humans and robots. The human are real humans with a political opinion, and the robots are algorithms on facebook trying to guess which political content it shouw display on the human's news feed.
   * The opinion of a given human is a real number between 0 and 1.
   * As for every CIRL game presented in the paper, there are two distinct phases : during the learning phase, the rebot show some political content to the human, asking them to choos their favorite. Thus, the robots tries to guess the political opinion of the human. This guess is called the *belief* of the robot, and is and interval between 0 and 1.
   * Then, during the deployment phase, the robot has several candidates available, and shows to the human the one which is supposed to be the closer to the human's opinion w.r.t. the robot's belief. As proved in the paper, this is the mean of the robot's interval.
   * The loss is the distance between the candidate presented during the deployment phase and the real opinion of the human. As it is a CIRL, the loss is the same for the human and the robot.
