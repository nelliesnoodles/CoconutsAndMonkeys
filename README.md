# CoconutsAndMonkeys
Playing with making some python methods to figure out math puzzle: coconuts and monkeys

## Quick intro:

Five pirates on an island start with a pile of coconuts of unknown quantity.
Each pirate sneaks out in turn at night, divides the pile up into 5 equal parts.
The pirate takes his 1/5 share out of the pile and hides it.
There is always 1 coconut remaining after this division, the pirate gives it to a monkey.
After all five have divided up the pile and hidden their share, and giving the monkey 1 remaining...
 
The pile in the morning is equally divisible by 5, with no remainder.  

## the plan:

Make a loop or recursion that can find the smallest original pile.  

## recurse_pile(pirates, original_pile, remainder, max=None):

 - pirates = number of pirates dividing the pile.
 - remainder = how many coconuts we're giving the monkeys
 - original_pile= where we want to start testing
 - max=None = set this number to below recursion amount.  about 2000 runs.

 So if our original pile is 3001, we'd set the max to around 5000
 or the function sets the max to (pirates ** pirates) + remainder.   It should only run twice in this instance (leaving max=None).
 
## run_pile(pirates, original_pile, remainder):

 - using a for loop, run through the pile by the number of pirates sorting through it.
 - on each for loop iteration, another function is called to reduce the pile accordingly.
 
## reduction(pile, pirates, remainder):
  
 - pile: passed in by the for loop in run_pile()
 - the new pile will be the pile arguement, minus the pirates share of the pile, and the remainder tossed to the monkey.
 - returns this new pile count. 

## Link
[wikipedia: The monkey and the coconuts](https://en.wikipedia.org/wiki/The_monkey_and_the_coconuts)






