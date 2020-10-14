# Summary

```{admonition} Order of Unions and Intersections
For events $A$ and $B$,
1. $P(A \cap B) = P(B \cap A)$
2. $P(A \cup B) = P(B \cup A)$
```

```{admonition} Contingency Table
A contingency table shows counts of cases on one categorical variable contingent on the value of another (for every combination of both variables).
```

```{admonition} General Rule
In general, for two events $A$ and $B$, $P(A|B) \not= P(B|A)$.
```

```{admonition} Marginal Probability
The unconditional probability on an event.
```

```{admonition} Joint Probability
The probability on simultaneous events.
```

```{admonition} Conditional Probability
The probability of an event given some other event. For two events $A$ and $B$, it
holds that:

1. $P(A|B) = \frac{P(A \cap B)}{P(B)}$, where $P(B) \not= 0$,
2. $P(B|A) = \frac{P(B \cap A)}{P(A)}$, where $P(A) \not= 0$.
```

```{admonition} Independence
Two events $A$ and $B$ are independent if $P(A \cap B) = P(B \cap A) = P(A) \cdot P(B)$

For independent events $A$ and $B$, combining the rules for conditional probability and independence yields:

1. $P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(A) \cdot P(B)}{P(B)} = P(A)$,
2. $P(B|A) = \frac{P(B \cap A)}{P(A)} = \frac{P(A) \cdot P(B)}{P(A)} = P(B)$,
```

```{admonition} Probability Tree
A probability tree is a graphical depiction of conditional probabilities.
```

```{admonition} Bayes’ Rule
$$
P(B|A) = \frac{P(A|B)\cdot P(B)}{P(A)}
$$

provided that $P(A) \not= 0$.
```

```{hint}
1. Presume events are dependent and use the General Multiplication Rule.
2. Use tables to organize probabilities.
3. Check that you have included all events.
```

```{caution}
1. Do not confuse $P(A|B)$ for $P(B|A)$.
2. Do not confuse counts with probabilities in contingency tables.
3. Understand that conditional probabilities are not shown in contingency tables, but can be calculated directly from them.
```

