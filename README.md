# Ai-learning-to-play-flappy-Bird
PPL Mini-Project Name: AI Learning to play flappy bird 
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Team: 
1) Aawesh – 111803146 
2) Ganesh – 111803139 
3) Saurabh – 111803145 
4) Shrijeet – 111803139 
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
The project consist of two parts as follows 
1) Creating the game 
2) The AI part 
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
1) Creating the game – Flappy Bird For creating the game we use the popular pygame module. First we import the required libraries and modules. We set the window width and height and create the window of the game. We give the name Flappy Bird to our game window. We create the variables for the images of components of the game and we join the images using the os module from the standard library. After that we create different classes for each component in the game.Then we create main function which has the loop for the game to be running. In each class we have functions for different activities in the game, like initialization, movement, and many other functionalities. Each class has the draw function which is used to draw the images on the window, these draw functions are used in the draw window function which is called in the main function.
2) The AI part For this we use the NEAT-Python module which is pure python implementation of NEAT. NEAT(NeuroEvolution of Augmenting Topologies) is an evolutionary algorithm that creates artificial neural networks. We maintain a population of individual genomes which contains two sets of genes that describe how to build artificial neural network namely: 
1) Node: genes which specify single neuron 
2) Connection: genes which specify connection between neurons To evolve the solution to problem, we have to provide a fitness function which computes single real number indicating the quality of each individual in the population.The algorithm then progresses through specific generations with each generation being produced by reproduction and mutation of fittest individual(s) of previous generation. The reproduction and mutation operations may add nodes and connections to genomes, so as the algorithm proceeds, genomes and the neural network produced by them may become more and more complex. When pre-defined number of generations is reached,or at least one individual exceeds the fitness threshold, the algorithm stops. In our project, we have kept the population of the genomes i.e. birds to be 100 and the fitness threshold is 100 meaning if any individual has fitness of 100 then the program will terminate. We have given points to make the bird go further in the game as below.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------
The AI works in our game as follows: 
1) If the bird hits the floor or the celling of the game window then its fitness is decreased and the bird is removed from the population. 
2) If the bird hits pipe then its fitness is decreased more and it is also removed from the population.
3) For each second the bird lives it gets 0.1 fitness points. 
4) If a bird passes through pipes then its fitness is increased by 2 fitness points. 
5) Always the new population of 100 birds or genomes is produced from the fittest individual bird in the previous generation, the fittest bird is the bird which has gone the most distance or which has crossed most number of pipes. 
6) In this way the new generation is capable of going through more number of pipes in each try. 
7) To make things more difficult, we have taken variable height pipes i.e. the position of the gap between the pipes will change with each new pipe added to the screen. 
8) To make it even more difficult, we have chosen that the gap between the pipes will also change i.e. it will be small sometimes and will be large sometimes.
