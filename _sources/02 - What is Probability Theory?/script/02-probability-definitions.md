# Probability Definitions

## Classical Probability

```{admonition} Classical Probability
$$
P(A) = \frac{\text{Number of outcomes that satisfy the event}}{\text{Total number of outcomes in the state space}}
$$
```

```{hint}
This method assumes all outcomes in the sample space to be equally likely to occur.
```


### Example: Cont’d: The Six-Sided Die

In this example, we throw a six-sided die. Recall that the state space $S$ is equal to $\{1, 2, 3, 4, 5, 6\}$.

```{dropdown} **Question**: What is the probability of getting a "6"?

**Solution**: All outcomes for throwing a six-sided die are equally likely (one can say in this case that the die is ‘fair’). Therefore we can use classical probability to determine this particular probability. In this example, $S$, i.e. the total number of outcomes, is equal to six. There is exactly one outcome that satisfies the event of getting a ‘6’ and this is rolling a ‘6’. Hence, the probability of getting a ‘6’ is exactly equal to $\frac{1}{6}\approx 0.167$
```

### Example: Cont’d: Roulette Wheel in Monte Carlo

Recall that the state space $S$ for a roulette wheel in Monte Carlo is equal to
$\{1, 2, ..., 35, 36, 0\}$.

```{dropdown} **Question**: What is the probability that the ball lands on a red number?

**Solution**: In this question, $S$ represents the state space that contains all possible outcomes of this random experiment. Every basket on the roulette wheel has the same size and hence all outcomes on the roulette wheel are equally likely. Therefore we can use classical probability to assess this particular probability. In this example, $S$ consists of 37 elements in total. There are 18 outcomes that satisfy the event of getting a red number. Hence, the probability that the ball lands on a red number is equal to $\frac{18}{37}\approx 0.486$
```

## Relative Frequency Probability

```{admonition} Relative Frequency Probability

$$
P(A) = \frac{\text{ Number of times the event A occurs in repeated trials}}{\text{Total number of trials in a random experiment}}
$$
```

```{hint}
$P(A)$ onverges to the true probability in the limit.
```

### Example: Combunox

Combunox is a drug that contains a combination of oxycodone and ibuprofen.  Oxycodone is an opioid pain medication. Ibuprofen is a non steriodal anti- inflammatory drug (NSAID). Combunox works by reducing substances in the body that cause pain, fever, and imflammation. During an experiment, it was reported that 49 out of 923 people vomited after taking Combunox.

```{dropdown} **Question**: What is the probability of vomiting after taking Combunox?

**Solution**: We want to determine the relative frequency that people vomited after taking combunox and therefore we can use relative frequency probability to determine this particular probability. The total number of trials in this random experiment is equal to 923. The number of times that people vomited is equal to 49. The probability of vomiting after taking Combunox is equal to $\frac{49}{923}\approx 5.3\%$
```

### Example: Google Stock Price

The end-of-day stock prices of Google are given in the figure below from
08-10-2019 to 08-10-2020 (which is equivalent to roughly 250 trading days).

```{image} images/google.png
:height: 300px
:name: image-die
```

```{dropdown} **Question**: Assume it is 08-10-2020. Based on the figure above, what is the probability that there will be a stock price increase on the next trading day?

**Solution**: In order to determine the state space initially, we need to determine all possible prices that the Google stock can attain.

- The minimum price of the stock is zero.
- The maximum price cannot be derived from historical stock price data with certainty.

We can define the following three events for the Google stock price change:

1. ‘Up’ (denoted by $u$), in case the stock price increases.
2. ‘Even’ (denoted by $m$), in case the stock price remains unchanged.
3. ‘Down’ (denoted by $d$), in case the stock price decreases.

Therefore the state space $S$ is equal to $\{u ,m, d\}$. Even though we defined the state space, it is impossible to determine the probability for each of the three elements in the state space, let alone for each price that is theoretically possible.
```

```{hint}
Hint: first determine the state space.
```

## Subjective Probability

```{admonition} Subjective Probability
An individual opinion or belief about the probability of occurence.
```

### Example: Steve Jobs
Steve Jobs had to use subjective probability in order to predict the probability of a success of the first iPad. There was no data available on which Steve Jobs could rely (except his experience and beliefs) and therefore he could not use relative frequency probability or classical probability. Considering the huge success of the iPad, Steve Jobs assessed this subjective probability quite well.

### Example: What is your Subjective Probability?

Linda is 31 years old, single, outspoken, and very bright. She majored in philosophy. As a student, she was deeply concerned with issues of discrimination and social justice, and also participated in anti-nuclear demonstrations.

**Question**: Which of the following eight options is more likely for Linda to be?

1. Linda is a teacher in elementary school.
2. Linda works in a bookstore and takes Yoga classes.
3. Linda is active in the feminist movement.
4. Linda is psychiatric social worker.
5. Linda is a member of the League of Women Voters.
6. Linda is a bank teller.
7. Linda is an insurance salesperson.
8. Linda is a bank teller and active in a feminist movement.
