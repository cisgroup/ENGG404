---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Independence 

## Introduction

Assume you throw a fair, six-sided die once. You write down the outcome and then you throw the die again.

```{dropdown} **Question 1**: What is the probability of getting a ‘1’ after the first roll?

**Solution**: The probability of getting a ‘1’ after the first roll is $\frac{1}{6}$.
```

```{dropdown} **Question 2**: What is the probability of getting a ‘2’ after the second roll, given that you got a ‘1’ after the first roll?

**Solution**: The probability of getting a ‘2’ after the second roll is completely unaffected by the outcome of the first roll. In other words, the probability of getting a ‘2’ after the second roll is independent from previous outcomes. Therefore the probability of getting a ‘2’ after the second roll is also equal to $\frac{1}{6}$.
```

```{dropdown} **Question 2**: What is the probability that you first roll a ‘1’ and then a ‘2’?


**Solution**: This question is slightly different from the previous question. In this question, we need to calculate $P('1' \cap '2')$. As determined in the previous question, both individual probabilities are equal to $\frac{1}{6}$. We can multiply the individual probabilities, because two subsequent rolls of a die are independent. Therefore we get $P('1' \cap '2') = P('1') \cdot P('2') = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36} (\approx 0.0278)$
```

## Independence

Two events $A$ and $B$ can be independent in the sense that the outcome of $A$ does not influence the outcome of $B$ and vice versa.

```{admonition} Multiplication Rule

Two events $A$ and $B$ are (statistically) independent if and only if the probability of both $A$ and $B$ occuring is the product of the probabilities of the two events $P(A \cap B) = P(A \,\text{and}\, B) = P(A) \cdot P(B)$.
```

## Examples

### Example: Game of Craps

Craps is a dice game in which the players make wagers on the outcome of the roll, or a series of rolls, of a pair of dice. Let us assume that there are two dice and that each player can bet on the sum of the two dice. Note that the sum is at least equal to 2 (a ‘1’ and a ‘1’) and at most equal to 12 (a ‘6’ and a ‘6’). The state space $S$ for the sum of the two dice is therefore equal to $\{2, 3, \dots, 11, 12\}$.

```{dropdown} **Question 1**: What is the probability that the sum is equal to the the minimum value (i.e. 2)?

**Solution**: The outcome of the first die is completely independent from the outcome of the second die. We know that the individual probabilities of getting for example a ‘1’ or a ‘6’ with either of the two dice is equal to $\frac{1}{6}$. Since the outcomes of the two dice are independent, we can use the multiplication rule. We get:

$$
P(\text{sum equals}\,2) = P('1' \cap '1') = P('1') \cdot P('1') = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36}
$$
```

```{dropdown} **Question 2**: What is the probability that the sum is equal to the maximum value (i.e. 12)?

**Solution**: The outcome of the first die is completely independent from the outcome of the second die. We know that the individual probabilities of getting for example a ‘1’ or a ‘6’ with either of the two dice is equal to $\frac{1}{6}$. Since the outcomes of the two dice are independent, we can use the multiplication rule. We get:

$$
P(\text{sum equals}\,12) = P('6' \cap '6') = P('6') \cdot P('6') = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36}
$$
```

```{dropdown} **Question 3**: What is the probability that the sum is equal to the the median value (i.e. 7)?

**Solution**: The outcome of the first die is independent from the outcome of the
second die. The outcomes of the first respectively the second die can be:
‘3 and 4’ or ‘4 and 3’ or ‘2 and 5’ or ‘5 and 2’ or ‘1 and 6’ or ‘6 and 1’.

Hence, there are in total six possible combinations of numbers that satisfy the event ‘sum equal to 7’ and there are 36 possible outcomes in total. Therefore $P(\text{sum equals}\,7) = \frac{6}{36} = \frac{1}{6}$.
```

```{dropdown} **Question 4**: What is the probability that the sum is equal to the second largest value (i.e. 11)?

**Solution**: The outcome of the first die is again independent from the outcome of the second die. The outcomes of the first respectively the second die can be: ‘6 and 5’ or ‘5 and 6’.


Hence, there are in total twp possible combinations of numbers that satisfy the event ‘sum equal to 11’ and there are 36 possible outcomes in total. Therefore $P(\text{sum equals}\,11) = \frac{2}{36} = \frac{1}{18}$.
```

### Example: Cont’d: Game of Craps

The probability distribution for the sum of two dice is not uniform (i.e. not each sum is equally likely to occur). We can simulate the outcomes of the two dice multiple times and see how often we get each sum.

```{code-cell} ipython3
---
tags: [hide-input]
---
import matplotlib.pyplot as plt
from numpy.random import randint as unif

trails = 500

A = unif(low=1, high=7, size=trails);
B = unif(low=1, high=7, size=trails);

plt.hist(A+B, facecolor='g', alpha=0.75);
```

```{admonition} Law of Large Numbers
:class: tip

It is clear from the simulation above that the probability that the sum equals 7 is far greater than the probability that the sum equals 2 or 3. If it were possible to do the simulation infinitly often, all probabilities will converge to their real exact probabilities. If we perform a large number of simulations (for example 1.000 or 10.000), we can already expect it to converge to quite accurate estimations of the true probabilities. This essentially means that in the long run, the relative frequency probability converges to classical probability. This principle is called the **law of large numbers**.
```

### Example: Apple Stock

Suppose that during the last 250 trading days, the Apple stock went up (denoted by $u$) on 150 days and went down (denoted by $d$) on 100 days. There were no days that the stock price of Apple remained unchanged and therefore we omit this event in this example. We assume that the probability of a future up movement respectively a future down movement of the stock price is equal to:

- $P(u) = \frac{150}{250} = 0.6$
- $P(d) = \frac{100}{250} = 0.4$

In addition we assume that the performance of the Apple stock price on the current trading day is independent of the performance of the Apple stock price on previous trading days. This means that the probability of an up or down movement from one day to the next is not affected by the number of previous up and down movements, e.g. if the Apple stock went up three days in a row, the probability that it goes up the next day remains unchanged.

In this question, we consider a week from Monday to Friday.


```{dropdown} **Question 1**: What is the probability that the stock price of Apple will increase on each consecutive day in the week?

**Solution**: There are five trading days in a week, so we need to calculate theprobability that there will be five subsequent up movements of the Apple stock price. It is given that each movement of the stock price is independent of the previous one. Therefore, we get by the multiplication rule:

$$
P(u \cap u \cap u \cap u \cap u) = P(u) \cdot P(u) \cdot P(u) \cdot P(u) \cdot P(u) = 0.6 \cdot 0.6 \cdot 0.6 \cdot 0.6 \cdot 0.6 = 0.6^5 \approx 0.078
$$

```

```{dropdown} **Question 2**: What is the probability that the Apple stock price will decrease on Monday, but subsequently will increase on Tuesday, Wednesday, Thursday and Friday?

**Solution**: Similar reasoning as for the previous question, we get by the multiplication rule:

$$
P(d \cap u \cap u \cap u \cap u) = P(d) \cdot P(u) \cdot P(u) \cdot P(u) \cdot P(u) = 0.4 \cdot 0.6^4 \approx 0.052
$$

```

```{dropdown} **Question 3**: What is the probability that the Apple stock price will decrease on either Monday, Tuesday, Wednesday, Thursday or Friday and will increase on the other four days?

**Solution**: The decrease could happen either on Monday, Tuesday, Wednesday, Thursday or Friday. As calculated in the previous question, the probability that the down movement happens on for example Monday is equal to 0.052. This probability does not depend on which day the down movement happens! Therefore, by using the multiplication rule for each scenario and summing these up, we get:

\begin{align}
& P(d \cap u \cap u \cap u \cap u) + P(u \cap d \cap u \cap u \cap u) +\\
& P(u \cap u \cap d \cap u \cap u) + P(u \cap u \cap u \cap d \cap u) +\\
& P(u \cap u \cap u \cap u \cap d) \approx 5 \cdot 0.052 = 0.26
\end{align}
```
