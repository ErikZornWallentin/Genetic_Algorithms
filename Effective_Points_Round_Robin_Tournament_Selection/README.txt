****************************************************
Erik Zorn-Wallentin	 Effective_Points_Round_Robin_Tournament_Selection.html
Friday, April. 8 / 2016
****************************************************

**********************
Compilation
**********************

JavaScript runs on a web browser so your file needs to be in .html ending format and open it in any web browser!

*********************************************************************
Running the program(s) and GENERAL INFO FOR ANY READER 
*********************************************************************

**IMPORTANT READ FOR USER**

The was created during my 3rd year of University.
This was part of a independent course project that I did during CIS*4900 class.

"Tournament selection is a method of selecting an individual from a population of individuals in a genetic algorithm.
Tournament selection involves running several "tournaments" among a few individuals (or 'chromosomes') chosen at random from the population. 
The winner of each tournament (the one with the best fitness) is selected for crossover." Quote from Wiki on Tournament Selection.

I am using this genetic algorithm as a potential use in my AI system, I will compare the results to other genetic algorithms before deciding which one I will use.
It will be compared against other genetic algorithms such as: FPS with fitness scaling, Tournament Selection, "Round Robinish" Tournament Selction, etc.
In some cases, I may use several different genetic algorithms or combined versions in my AI system, but that has yet to be decided.

See wiki for more info: https://en.wikipedia.org/wiki/Tournament_selection

In plain words, RR.TS(Round Robin Tournament selection) first sorts from best to worst.
After it will choose the best monster and compare it against alpha as the chance to lose using a randomly generated number.
If the target wins against alpha the algorithm stops and the best monster is chosen, but if alpha wins it will move onto the next best monster in the list to compare against.
The cycle continues until no more targets are left and it displays a winning / losing target that is dependent on alpha.

I use the wiki as my reference for my project, and added a few modifications to it.
I fully understand this code as I wrote it and I am able to describe it to a "non-programmer" if requested.

Pseudo code:
	The algorithm: (pChooseWorst)
	1) Sort the monsters from highest probability to lowest
	2) monsterChoice = 1
	3) randomNum = random number between 0 and 1
	4) if randomNum > pChooseWorst
   return monsterChoice
	5) monsterChoice = monsterChoice + 1
	6) if monsterChoice = numOfMonsters
		return monsterChoice
	7) Go to step 3


Feature's: Takes 4 target's and chooses the target based on the alpha value given.
		   There is support to accept only the highest one too, just click on the check box for it to only choose the highest one! 
		   In the case of a tie it will choose the last one found.
		   Also takes an alpha modifier which allows you to reduce or increase the alpha probability after each "round".
		   
Based on my AI system we will compare the pro's and con's of using this system:
	Pro:
		- Extremely "tunable" to perfectly support "dumb/smart" AI.
		- Allows targets with 0 probability/EP to be chosen based on alpha value.
		- Most efficient way for the AI to find a target based on the system we need while still being "tunable".
	Con:
		- Need to add modifications as it's sometimes hard to get the "2nd best / 2nd worst" target when probability is closer to 0.5,
		  this was fixed by adding alpha modifier.

AI Info: We gather Effective Points on each target, this is based on a different system and this system only cares about calculating those effective points.
         The targets with higher effective points will have higher probabilities. We want the monster with the highest probability to be chosen.
		
Example Use 1:
	First Target: 1
	Second Target: 20
	Third Target: 40
	Fourth Target: 1000
	Alpha( 0-1 ): 0.2
	Alpha Modifier ( 0-1 ): 0.1
	Always pick highest Target: NOT CHECKED
	
	--- OUTPUT ---
	Target Chosen: Fourth Target -- 1000  ( most likely output )
	Probabilities Used: 0.20
	
Example Use 2:	
	First Target: 66
	Second Target: 55
	Third Target: 74
	Fourth Target: 1
	Alpha( 0-1 ): 0.4
	Alpha Modifier ( 0-1 ): 0.1
	Always pick highest Target: NOT CHECKED
	
	--- OUTPUT ---
	Target Chosen: Third Target -- 74 ( most likely output )
	Probabilities Used: 0.40

**************************
Bibliography / References
**************************

https://en.wikipedia.org/wiki/Fitness_proportionate_selection
https://en.wikipedia.org/wiki/Tournament_selection


*****************
Known Limitations
*****************

NONE

