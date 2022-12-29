# NimGame
Finding the best strategy to win the Rim game!

"""
Our player's strategy is formulated into three parts which differ depending on the number of non-empty piles
that remain in the list. When there are more than two non-empty piles in the list, we clear out an entire pile 
at a time. This is because if we can only pick from one pile every turn given the rules of the nim game, we can be sure 
neither player is capable of winning if more than two non-empty piles exist in the list. The second part which is also a
straight forward course of action occurs when there exists only one non-empty pile in the list. In this case, we would
clear out all the coins in that list, which would ensure our player wins, given that this is the last non-empty pile
left. What is more tricky is when there are exactly two non-empty piles left in the game. Our strategy in this case is 
to make sure the piles maintain an even number of coins. If there are an even number of coins in the pile, we subtract 
two coins to keep the pile even. If there are an odd number of coins in the pile, we subtract one to make the pile newly
even.

Much of our thought process for this project was done on scratch paper. We first quickly came to the conclusion that 
what our program does before there are only two non-empty piles left is not very important. Initially we were planning 
on having our program randomly pick a pile and remove a random number of coins from that pile but decided it would be 
simpler to clear out an entire pile at a time. Then, we spent much of our time sketching hypothetical nim game states on 
paper, mainly testing between three states: 1. Two piles, both having an even number of coins 2. Two piles, both having 
an odd number of coins 3. Two piles, one having an odd number of coins and one having an even number of coins. We had 
two team members play the game several times to find patterns in methods used to win the game. What we found was that 
when a player was left with a total of two coins in the game (1 coin in one pile and 1 coin in the other), it was 
inevitable that they lose. This is because they would be forced to pick a coin from one pile, leaving the other player 
with the last coin. Thus, our strategy involved keeping the piles even to avoid such a situation. We also found that 
taking the smallest possible number of coins at a time (either 2 or 1 depending on whether the pile is even or odd, 
respectively), was the most rational move our own program could make. Taking larger amounts of coins in our hypothetical 
situations often gave the other player leverage to manipulate the stacks and be left with the last non-empty pile. Taking 
the smallest possible number of coins every turn increased the other player's room for error, such as clear out the second 
to last non-empty stack and leaving us with the last non-empty stack (which we clear out to win the game). Thus, keeping
the stacks even and removing the smallest number of coins possible makes our program play on the safer side of the nim game 
and rely on error from the other player.
