## Chapter 1: Introduction
We mainly cover:
1. Probability model
2. Commonly used random variables

### 1.1 Basic concepts of probability model
- Probability model
3 components of a probability model:
    - Sample space
    - Event
    - Probability function
- Sample space:
All possible outcomes of a random experiment.
    >e.g. Toss a coin twice: $S = \{(H,H), (H,T), (T,H), (T,T)\}$
- Event
Roughly speaking: Event = subset of the sample space.
    >e.g. E=$\{(H,H)\}$, subset of sample space $S$.
- Probability function
Notation $P$. Probability function is a function of event and satisfies 3 conditions:
    1. $0 \leq P(E) \leq 1$ for any event $E$
    2. $P($Sample Space$) = 1$
    3. Suppose $E_1, E_2, \dots$ are a sequece of disjoint events, i.e. $E_i \cap E_j = \emptyset$(empty set) for $i \neq j$. Then $P(\bigcup_{i=1}^{\infty} E_i) = \sum_{i=1}^{\infty} P(E_i)$ [Additivity Property]
        > e.g. Toss coin twice
        Define $P(E)=\frac{\text{\# of outcomes in }E}{4\text{ (Total \# of outcomes in sample space)}}$
        >>Exercise: Verify $P$ is a probablity function

- Property of probability function
    1. If $E_1 \subset E_2$, then $P(E_1) \leq P(E_2)$
        - If $E1$ occurs, then $E_2$ must occur $\implies E_1 \subset E_2$.
        - If $E_1$ implies $E_2$, then $E_1 \subset E_2$.
    2. If $E_1 \cap E_2 = \emptyset$, then $P(E_1 \cup E_2) = P(E_1) + P(E_2)$
    3. $P(\emptyset) = 0$
    4. $P(E) + P(E^c) = 1$
        - $E^c$ is the complementary of $E$.
    5. $P(E_1 \cup E_2) = P(E_1)+P(E_2)-P(E_1\cap E_2)$

- Independence
Two events $E$ and $F$ are independent if $P(E \cap F) = P(E) \cdot P(F)$ where $P(E \cap F)$ is the joint probability and $P(E) \cdot P(F)$ is marginal probabilities or unconditional probabilities.
so, independence means:
<center>joint = product of marginals</center>

- A useful result
Suppose we have a sequence of independent trials and a sequence of events $E_1, E_2, \dots$.
Now: $E_i$ only depends on $i$th trial $\implies$:
    1. all events $E_1, E_2, \dots$ are independent
    2. $P(\bigcap_{i=1}^{\infty} E_i)= \prod_{i=1}^{\infty} P(E_i)$
    2. $P(\bigcap_{i=1}^{m} E_i)= \prod_{i=1}^{m} P(E_i)$



>Example 1.1 (Independent Example):
Suppose the die is a fair die. If you repeatedly and independently toss a die, then you will get a sequence of numbers.
Find:
>1. $P($getting a "3" in the sequence of numbers$)$
    >>Solutions:
    >>Let $E$ = "3" in the sequence
    >>$E^C$ = No "3" in the sequence
    >>Then, $$P(E^C) = P(1\text{st} \neq 3 \cap 2\text{nd} \neq 3 \cap 3\text{rd} \neq 3 \cap \dots) \\ = \prod_{i=1}^\infty P(i\text{th} \neq 3) = \frac{5}{6}^\infty = 0$$
>2. $P($getting a "333" in the sequence of numbers$)$
Here we say "333” occurs on the $n$th toss if the $(n-2)$th outcome is "3”, $(n-1)$th outcome is "3”, and $n$th outcome is "3”.
>> Solution: Let $F$ = "333" in the sequence
>> $F^C$ = No "333" in the sequence
>> Idea: Create independent blocks of 3 tosses.
>> Note: $F^C$ implies that $\text{block }1 \neq "333", \text{block }2 \neq "333", \text{block }3 \neq "333", \dots \implies$ $F^C \subset \{\text{block }1 \neq "333", \text{block }2 \neq "333", \text{block }3 \neq "333", \dots\}$


>Example 1.2:
A coin is continually and independently tossed, where the probability of head (H) on a toss is $1/2$.
Find:
>1. $P(1$st two tosses give "HH"$)$
>2. $P(1$st two tosses give "TH"$)$
>3. $P($"TH" occurs before "HH"$)$