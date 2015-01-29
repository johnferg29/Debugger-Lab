## John Ferguson's Answers to Lab 2
**Question 1:** Why is `cutoff` not a parameter to the method `playTurn` in the `PigGame` class?

**Answer 1:** The reason `cutoff` is not a parameter to the method `playTurn` in the `PigGame` class becasue `cutoff` lets you know that value at which you stop playing the game.  If you set `cutoff` to `playTurn` then you're giving yourself a certain amount of turns and that doesn't work.  You don't know how many turns it will take to get to the `cutoff` value.

**Question 2:** What would the following code print? `ScoreShet s = new ScoreSheet(); System.out.print.ln(s.getTurnAverage());`

**Answer 2:** This code is printing out the average number of turns played on a new scoresheet that we created.

**Question 3:** In the `PigGame` class, `numBusts` is inceremeneted in the `playGame` method.  Describe how this statement could be moved to another methond in the class without affecting the results.

**Answer 3:** numBusts can be moved into playTurn without affecting the results.  But within playTurn it would have to be placed after rolledOne = true because then we know we rolled a 1 and we busted so now we can add 1. 

**Question 4:** Based on your current understanding of the code, where do you think the problems might be located? Are there portions of the code where you are fairly certain the problems could not possibly be?

**Answer 4:** Based on my current understanding of the code, I think that the reason the code is stuck in an infinite loop is becasue all we told the code to do is playGame.  We didn't give any other information to track any values or numTurns either.  So all the code is doing right now is playing the game infinitely. It doesn't know when it's getting to the cutoff value. On the other hand I think there can't be any problems where we created a new game becasue we gave the new game a cutoff value, also the print statements.

**Question 5:** Describe the problems with the program and the ways you made the program execute correctly.

**Answer 5:** The problem was in Die.Java. In the upValue loop, the int was in the wrong spot.  It was making the random numbers only select from 0 to 1 instead of 1 t0 6 becasue of that. Then I put int infront of the right side so it looked like (int)(Math.random() * 6)+1;.

**Question 6:** Using the correct program, what are teh average number of turns for cuttoff values 10,15,20,25?

**Answer 6:** 
10 : 11.2
15 : 5.611111
20 : 6.4375
25 : 17.0

	   