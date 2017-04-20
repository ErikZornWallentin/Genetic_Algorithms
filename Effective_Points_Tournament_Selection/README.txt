****************************************************
Erik Zorn-Wallentin	 Effective_Points_Tournament_Selection.html
Thursday, April. 7 / 2016
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

In plain words, TS(Tournament selection) selects "n" amount of targets to be selected,
where the highest probability among the randomly "n" selected wins.

I use the wiki as my reference for my project, and added a few modifications to it.
I fully understand this code as I wrote it and I am able to describe it to a "non-programmer" if requested.

Feature's: Takes 4 target's and chooses the target based on the highest probability that was selected as 'n' number of selections.
		   There is support to accept only the highest one too, just click on the check box for it to only choose the highest one! 
		   In the case of a tie it will choose the last one found.
		   
Based on my AI system we will compare the pro's and con's of using this system:
	Pro:
		- Allows the possibility of lower probabilities to win, which is "tunable" .
	Con:
		- Not a useful to use when I make the AI "dumb" or when AI is "super smart" as it will generally not accept the correct target that I want.
		- If a probability is 0, we will never get that as a chosen value (which we do not want, but we need it still as an option).

AI Info: We gather Effective Points on each target, this is based on a different system and this system only cares about calculating those effective points.
         The targets with higher effective points will have higher probabilities. We want the monster with the highest probability to be chosen.
		
Example Use 1:
	First Target: 1
	Second Target: 20
	Third Target: 40
	Fourth Target: 1000
	Amount Selected(1-4): 3
	Always pick highest Target: NOT CHECKED
	
	--- OUTPUT ---
	Target Chosen: 4 - Most likely ( as long as 4 was among the randomly selected)
	
Example Use 2:	
	First Target: 66
	Second Target: 55
	Third Target: 74
	Fourth Target: 1
	Amount Selected(1-4): 3
	Always pick highest Target: CHECKED
	
	--- OUTPUT ---
	Target Chosen: 3

**************************
Bibliography / References
**************************

https://en.wikipedia.org/wiki/Fitness_proportionate_selection
https://en.wikipedia.org/wiki/Tournament_selection
https://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle


*****************
Known Limitations
*****************

NONE

