****************************************************
Erik Zorn-Wallentin	 Fitness_Proportionate_Selection.html
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

" Fitness proportionate selection, also known as roulette wheel selection, 
is a genetic operator used in genetic algorithms for selecting potentially useful solutions for recombination."

I am using this genetic algorithm as a potential use in my AI system, I will compare the results to other genetic algorithms before deciding which one I will use.
It will be compared against other genetic algorithms such as: FPS with fitness scaling, Tournament Selection, "Round Robinish" Tournament Selction, etc.
In some cases, I may use several different genetic algorithms or combined versions in my AI system, but that has yet to be decided.

See wiki for more info: https://en.wikipedia.org/wiki/Fitness_proportionate_selection

In plain words, FPS(Fitness proportionate selection) sums up the probabilities and chooses one of the probabilities,
where if one probability is much higher than the rest it is more likely to be chosen. In the case of probabilities being close to each other,
you will have different results more easily and won't always choose the same value.

I use the wiki as my reference for my project, and added a few modifications to it.
I fully understand this code as I wrote it and I am able to describe it to a "non-programmer" if requested.

Feature's: Takes 4 targets and the AI will choose the target based on their probabilities. 
		   There is support to accept only the highest one too, just click on the check box for it to only choose the highest one! 
		   In the case of a tie it will choose the last one found.
		   
Based on my AI system we will compare the pro's and con's of using this system:
	Pro:
		- The one with highest probability usually gets selected, 
		  and if it is much higher than the others it will almost always get selected.
		- Efficient.
		- Fitness scaling can help "ease" the results, for example if we add a million to each probability it will make all values "more closer" 
		  and that way our choices are more equal.
	Con:
		- Not a useful to use when I make the AI "dumb" and I want the AI to choose one of the "weaker" options.
		- If a probability is 0, we will never get that as a chosen value (which we do not want as we need it still as an option),
		  Fitness scaling can solve this (raise 0 value, and raise everything else by same amount).
		- Negative values will not work (fitness scaling can also solve this).
		
Example Use 1:
	First Target: 0.001
	Second Target: 0.01
	Third Target: 0.04
	Fourth Target: 0.99
	Always pick highest target: NOT CHECKED
	
	--- OUTPUT ---
	Target Chosen: 4 - Most Likely!
	
Example Use 2:	
	First Target: 0.66
	Second Target: 0.55
	Third Target: 0.74
	Fourth Target: 0.01
	Always pick highest: CHECKED
			
	--- OUTPUT ---
	Target Chosen: 3

**************************
Bibliography / References
**************************

https://en.wikipedia.org/wiki/Fitness_proportionate_selection
https://en.wikipedia.org/wiki/Tournament_selection


*****************
Known Limitations
*****************

NONE

