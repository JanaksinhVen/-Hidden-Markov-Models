# Hidden-Markov-Models
The question answer format repository for  Hidden Markov Models.

Hidden Markov Models (HMMs) are powerful statistical models widely used
in various fields such as speech recognition, bioinformatics, and finance. They
are particularly effective for modeling sequences of observations with underlying
hidden states. HMMs belong to the family of probabilistic graphical models and
are characterized by their simplicity and versatility.
## Basic Components
An HMM is composed of the following basic components:
1. States (S): A set of hidden states that the system can be in at any given
time. These states are not directly observable.
2. Observations (O): A set of observable symbols or emissions associated
with each hidden state.
3. Transition Probabilities (A): The probabilities of transitioning from
one hidden state to another. Represented by a matrix A, where Aij is the
probability of transitioning from state i to state j.
4. Emission Probabilities (B): The probabilities of observing a particular
symbol given a hidden state. Represented by a matrix B, where Bij is the
probability of emitting symbol j from state i.
5. Initial State Probabilities (π): The probabilities of starting in a particular hidden state. Represented by a vector π, where πi
is the probability
of starting in state i.
## Modeling Process
The process of modeling with an HMM involves the following steps:
1. Initialization: Assign initial values to the transition probabilities, emission probabilities, and initial state probabilities.
2. Forward Algorithm: Compute the probability of observing a sequence
of symbols given the model.
3. Backward Algorithm: Compute the probability of being in a particular
state given the observed sequence.
4. Expectation-Maximization (EM) Training: Adjust the model parameters to maximize the likelihood of the observed data.

## Applications
HMMs find applications in a variety of domains:
• Speech Recognition: Modeling phonemes and words.
• Bioinformatics: Predicting protein structures and gene locations.
• Finance: Analyzing financial time series data.
• Robotics: Tracking the movement of objects.
## Task-1
You are Chottu, a casino inspector, whose job is to investigate whether a casino
is trading out a fair die for a loaded (unfair) die and scamming the customers.
At the same time, you are also well-versed in Statistical Methods in Artificial
Intelligence, and you realize that you can use Hidden Markov Models to solve
this case. You need not implement the HMM from scratch but are allowed to use
any standard library. But please make sure you are familiar with the underlying
theoretical concepts.
### Dataset
You are provided with a file named rolls.npy, a NumPy file containing data
from 50,000 observed rolls at the casino. Each roll is represented by the number
on the top face of the die. For instance, if the number 5 is recorded, it indicates
that a 5 was rolled. Also, assume that the first die was a fair one.
### Part 1
1. Train an HMM model with a 50 % train and validation split (Split it
sequentially, that is the first 50 % rolls should be on the train set and rest
in validation. Experiment with different emission probabilities for the
loaded die and report the model with the best score. Use the validation
split to evaluate the best model.
2. Find the most likely sequence of switching between the fair and loaded
die.
3. Plot the generated states.
4. What problem in Hidden Markov Models does this task correspond to?
### Part 2
1. How often do you think the casino is switching out the fair die for the
loaded one and vice versa?
2. What problem in Hidden Markov Models does this task correspond to?

### Part 3 
1. How do you think the loaded die is biased
2. What problem in Hidden Markov Models does this task correspond to?
Note: Use a random seed of 13 in the entire exercise.
## Task-2 : 
Virat and Rohit are opening the batting for India. You are following the game on
the radio. The local radio station’s ball-by-ball commentator speaks a language
you can’t understand, but you can figure out the runs scored for each ball and
that both openers played the entire match.  

ICC has a new rule: there are no more batsman changes for odd runs or at
the end of each over. However, there’s a 30 percent chance you won’t know the
exact number of batsman changes at the end of each ball.  

As a cricket enthusiast, you know Virat is likely to focus on singles and doubles
to anchor the innings. In contrast, Rohit is more prone to taking risky shots to
boost the run rate.  

Dataset: You are provided with runs.npy which contains a sequence of length
30000 representing the runs scored by the players for each ball. The possible
runs scored for a ball is 0,1,2,3,4,6. Assume there were no 5 runs scored.
1. Find the optimal transition, emission and start probability for the HMM
model.
2. Choosing the best HMM based on the data, and the model information
can you predict who played the first and the last ball?
