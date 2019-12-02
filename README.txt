Name: Shreif Abdallah
NetID: selsaid
Partner Name : Meiwen Zhou
NetID: mzhou26


Compile instructions :-

javac Dining.java

Running instructions :-

1- Verbose output

java Dining -v

2- No output

java Dining 


After 10 minutes of testing, we did not see a deadlock, when analyzing our results we arrived at the following distibution.

(included in output.txt is the output that we got after testing)

Correctness check passed!
Fairness breakdown:
                Think   Wait    Eat
Philosopher 1:  38.0%   37.7%   24.3%
Philosopher 2:  36.3%   39.6%   24.1%
Philosopher 3:  37.7%   39.1%   23.2%
Philosopher 4:  36.8%   38.2%   25.0%
Philosopher 5:  36.9%   38.2%   24.9%


Solution discussion :-

Our solution was to begin by ensuring that no two philosophers were using the same fork, by adding an extra parameter labeled inUse, which is a boolean variable that is true when the fork is being used, and false when the fork is released. 

We attempt to recover from deadlocks by ensuring -slightly- randomized wait times before attempting to grab the fork, that means that waiting, eating, thinking cycles are not in sync, and we won't end up with a situation where everyone grabs one chopstick at the same time.

Our results show that all philosophers are eating equally, and are also waiting equally. And also starvation-free, since all philosphers eat at some point.

Extra credit: 
Using prettier graphics for philosopher and fork objects.




