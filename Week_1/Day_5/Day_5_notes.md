# Day 5 Notes
## Recursion
Example:
```
1.| function countEvenToTwelve(number) {
2.|   if (number <= 12) {
3.|     console.log(number);
4.|     countEvenToTwelve(number+2);
5.|   }
6.| }
7.| countEvenToTwelve(0);
```
Consists of at least one base and one recursive case in order to be recursive.
*Base case*: Condition on which, if true, the function will not call itself.
*Recursive case*: As long as this condition is true, the function will continue to call itself.

Each recursive  call should break down the current problem into a smaller, simpler one. It must eventually reach the smallest version of the problem, the base case, where the problem can be solved without further recursion.

*Hint*:  The unknown number of nested loops is a common characteristic of all problems that are recursive in their nature and should give you a hint that recursive solution is required.

## Helpful Links
[Dijkstra was right -- recursion should not be difficult](https://blog.angularindepth.com/learn-recursion-in-10-minutes-e3262ac08a1) 