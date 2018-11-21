Sum23

 

1.      The goal of this project is to apply reinforcement learning methods to a simple card game that we call Sum23. Here is a list of the rules of the game.

 

·        The game is played with one dealer and one player.

·        The game is played with an infinite deck of cards with heart (red), diamond (red), and club (black) (i.e. cards are sampled with replacement)

·        Each draw from the deck results in a value between 1 and 10 (uniformly distributed) with a color of red (probability 2/3) or black (probability 1/3).

·        There are no face cards in this game.

·        Ace card is always just one.

·        At the start of the game, both the player and the dealer draw one red card (fully observed). If the first card is club (black), just discard and draw a new one until it is either heart or diamond.

·        Each turn the player may either stick or hit.

·        If the player hits then the player draws another card from the deck.

·        If the player sticks then the player receives no further cards.

·        The values of the player's cards are added (red cards) or subtracted (black cards)

·        If the player's sum exceeds 23, or becomes less than 1, then the player goes bust and loses the game (reward -1)

·        If the player sticks then the dealer starts taking turns. The dealer always sticks on any sum of 18 or greater and hits otherwise. If the dealer goes bust (sum exceeds 23, or becomes less than 1), then the player wins; otherwise, the winner will be the one with the largest outcome. {win (reward +1), lose (reward -1), or draw (reward 0)}

 

 

2.      Implementation of Sum23

·        It is model-free reinforcement learning, so you should not explicitly compute or represent the transition matrix for the MDP. There is no discounting. You should treat the dealer's moves as part of the environment, i.e. a stick action of the player will play out the dealer's cards and return the final reward and terminal state.

·        You should write an environment that implements the MDP of the game. Specifically, write a function that takes as input a state s (dealer's first card 1-10 and the player's sum 1-21), and an action a (hit or stick), and returns a sample of the next state s’ (which may be terminal if the game is finished) and reward r.

 

3.      Monte-Carlo Reinforcement Learning (50 scores for graduate students and 100 scores for undergraduate students)

·        Initialize the state-action value function to zero. Please plot the computed optimal state-action value function in a similar way to draw the optimal state-action value function for Blackjack example. (refer textbook Figure 5.1 on page 77)

·        Textbook: An Introduction to Reinforcement Learning, Richard S. Sutton and Andrew G. Barto, Second edition, in progress (Available free online! http://incompleteideas.net/book/bookdraft2017nov5.pdf)

 

4.      TD Reinforcement Learning (50 scores for graduate students and 100 scores for undergraduate students)

·        Initialize the state-action value function to zero. Implement both 1-step Sarsa and Q learning. Please plot the computed optimal state-action value function in a similar way to draw the optimal state-action value function for Blackjack example.

 

5.      Linear Function Approximation (30 extra scores for all students)

 

6.      Submission

·        Please submit a single pdf report containing your plots and simple discussion of your implementations of each algorithm including how you set the step size and the greedy exploration, and a single archive containing all your source code.

·        Please organize your source code so that it is easy to follow and run.

·        Send your submission to Moodle.

·        The deadline for the project is Thursday, Dec. 6 at 11:00 pm.

·        This project should be completed individually

