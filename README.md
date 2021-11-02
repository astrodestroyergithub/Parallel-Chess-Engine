# Parallel-Chess-Engine
A chess engine made using the Negamax implementation of the MiniMax algorithm, and optimized using Alpha-Beta pruning.

## Abstract:
Computer chess has been a compelling research topic since the very inception of the artificial intelligence field. Although newer search algorithms have been proposed, some with great success, the venerable alpha-beta algorithm remains at the heart of most implementations. Augmenting alpha-beta with heuristic enhancements and knowledge databases has extended its power considerably. We will investigate the most basic serial chess algorithms and techniques for parallelizing them and will also try to present an extremely simple implementation aimed at small-scale, commodity SMP workstations. We will be using the Negamax implementation of the MiniMax algorithm for playing the game, and later will be using Alpha-Beta pruning to reduce the execution time of our code and for optimization.

## Architecture:
We are going to design a chess engine by employing the Negamax implementation of the Minimax algorithm and then optimizing it with Alpha-Beta Pruning, and then compare it to the previous one by simulating chess games at different depths between the engine and its improved version. But first things first, before we start parallelizing stuff, we must find an algorithm that allows this parallelization while still taking advantage of the alpha-beta pruning technique. We have to parallelize the moves of the 2 players. The player 1 will accept the inputs of α and the player 2 will accept the inputs of β. At each alternating step, we have to maximize the player 1’s moves (α) and minimize the player 2’s moves (β). Finally, based on the best choices, for each, a final optimized solution will be achieved. Finally, Heuristic enhancements will lead to the optimization of the parallel chess algorithm. The various modules and functions will help in implementing the Alpha-Beta pruning.

## Description:
It is a simple chess game which runs on flask server. It is equipped with one built-in chess engine named devzero (where 'dev' stands for developer and 'zero' stands as an ending which many chess engines have such as alphazero and leelazero) developed by me and three other uci compatible chess engines named stockfish, cdrill and deuterium for learning purposes. It has an assistant which gives the user some introduction, instructions and credits. It also warns the user when it is check and also when it is a checkmate or stalemate. This game can be played on two different devices by port forwarding your local host port or by the ngrok tool available for windows, mac and linux. But as it is running on a flask server it doesn't have any restrictions means anyone can play anymove, at anytime.

## Requirements
You can run the `setup.py` by which all the modules will be downloaded automatically by pip:
```
python setup.py
```
Or you can do it manually by executing the following commands:
```
pip install python-chess
```
```
pip install flask
```
```
pip install pyttsx3
```
```
pip install webbrowser
```
## Execution
Run the following code in your terminal:
```
python play.py
```
## Features
> 1. Voice Assistant
> 2. Follows all chess rules
> 3. Four Compatible Chess Engines
> 4. Can be played on two different devices
# Playing over the internet
You can use the tool [ngrok](https://ngrok.com/download) for playing it in two different places of the world. Just download it, cd into the following directory and type the following code:
```
ngrok http 5000
```

_For improving the smartness of our algorithm, some of the initial set of moves which we will be using are present in .bin format. Theese moves are normally used by many chess grandmasters as their opening moves. Get some of them_ [Here](https://github.com/astrodestroyergithub/Parallel-Chess-Engine/tree/master/books)

## References:
* https://towardsdatascience.com/ai-in-chess-the-evolution-of-artificial-intelligence-in-chess-engines-a3a9e230ed50
* https://subscription.packtpub.com/book/application_development/9781785289583/1/ch01lvl1sec14/how-to-evaluate-the-performance-of-a-parallel-program
* https://www.geeksforgeeks.org/minimax-algorithm-in-game-theory-set-1-introduction/
* https://www.javatpoint.com/ai-alpha-beta-pruning
* https://www.sciencedirect.com/science/article/pii/0893965996000110
* https://www.geeksforgeeks.org/iterative-deepening-searchids-iterative-deepening-depth-first-searchiddfs/
