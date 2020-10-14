# Probability Types

## Marginal, Joint and Conditional Probabilities

```{admonition} Marginal Probability

The marginal probability is the unconditional probability on an event. This probability is not conditioned on any other event. 

Notation: The marginal probabilities of two arbitrary events $A$ and $B$ is denoted by respectively $P(A)$ and $P(B)$.
```

```{admonition} Joint Probability

The joint probability is the probability of simultaneous events. This is the probability of the intersection of two or more events. 

Notation: The joint probability of two arbitrary events $A$ and $B$ is denoted by
$P(A \cap B)$.
```

```{admonition} Conditional Probability

The conditional probability is the probability of an event given that some other event has occured. The information from the event that has occured can influence the probability of the original event.

Notation: For two events $A$ and $B$, the conditional probability of $A$ given $B$ is denoted by $P(A|B)$ and the conditional probability of $B$ given $A$ is denoted by $P(B|A)$.
```

```{attention}
In general, for two arbitrary events $A$ and $B$, $P(A|B) \not= P(B|A)$.
```


Figure {numref}`figure-venn-old` shows the ‘old’ sample space $S$ for two events $A$ and $B$. Note that there is an overlap between $A$ and $B$.

```{figure} images/venn-old.png
:height: 200px
:name: figure-venn-old

"old" sample space $S$
```

Figure {numref}`figure-venn-new` shows the ‘new’ sample space $S$ for two events $A$ and $B$ , because it shows the relation with respect to conditional probabilities. The conditional probability can be calculated by dividing the probability of the dark blue area ($P(A \cap B)$) by the probability of the light blue area ($P(B)$). Note that the area of $A \cap B$ can be at most as large as the area of $B$ (which is the case if $B$ is fully contained in $A$). Therefore, if we calculate the conditional probability $P(A|B) = \frac{P(A \cap B)}{P(B)}$, we immediately have that $P(A|B)$ is smaller than or equal 1.

```{figure} images/venn-new.png
:height: 200px
:name: figure-venn-new

"new" sample space $S$
```

```{admonition} Proof of $P(A|B) \not= P(B|A)$
:class: dropdown

Assume that:

- $P(A) \not= P(B)$, $P(A) \not= 0$ and $P(B) \not= 0$.

We get:

$$
P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{P(B \cap A)}{P(B)} \not = \frac{P(B \cap A)}{P(A)} = P(B|A)
$$

where we used in the second last step that $P(A) \not= P(B)$.
```

## Examples

Consider the internet shopping example we saw earlier. Recall that the contingency table showed the following pieces of information:

- The website through which a customer ended up at Amazon.com
- Whether the customer made a purchase or not

The probability types that are given in a table corresponding to the contingency table are always

- The marginal probabilities
- The joint probabilities

The conditional probabilities can be calculated based upon these marginal and joint probabilities.

In the table below, the marginal probabilities are visible in the column ‘Total’ and the row ‘Total’. The joint probabilities are visible in the columns ‘MSN’, ‘Recipe Source’ and ‘Yahoo’ and the rows ‘NP’ and ‘P’.

```{list-table}
:header-rows: 1
:name: table-amazon-3

* -
  - MSN
  - Recipe Source
  - Yahoo
  - Total
* - P
  - $P(\text{MSN} \cap \text{P})$
  - $P(\text{Recipe Source} \cap \text{P})$
  - $P(\text{Yahoo} \cap \text{P})$
  - $P(\text{P})$
* - NP
  - $P(\text{MSN} \cap \text{NP})$
  - $P(\text{Recipe Source} \cap \text{NP})$
  - $P(\text{Yahoo} \cap \text{NP})$
  - $P(\text{NP})$
* - Total
  - $P(\text{MSN})$
  - $P(\text{Recipe Source})$
  - $P(\text{Yahoo})$
  - $1$
```

```{dropdown} **Question**: Consider again the internet shopping example that we saw earlier. Customers from which website are most likely to make a purchase on Amazon.com?

**Solution**: The table below shows again the data (in terms of probabilities) for web shopping at Amazon.com. The table shows the website through which a customer ended up at Amazon.com and whether the customer made a purchase or not.

| | MSN | Recipe Source | Yahoo | Total |
| --- | --- | --- | --- | --- | --- |
| No Purchase| 0.396| 0.243| 0.332| 0.971 |
| Purchase| 0.016| 0.000| 0.013| 0.029 |
| Total| 0.412| 0.243| 0.345| 1.0 |

In the question it is given that the customer made a purchase. Therefore we need to calculate the following probabilities:

- $P(\text{MSN} | \text{Purchase}) $
- $P(\text{Recipe Source} | \text{Purchase}) $
- $P(\text{Yahoo} | \text{Purchase}) $

We get:

$$
P(\text{MSN} | \text{Purchase}) = \frac{P(\text{MSN} \cap \text{Purchase})}{P(\text{Purchase})} = \frac{0.016}{0.029} \approx 0.552
$$

$$
P(\text{Recipe Source} | \text{Purchase}) = \frac{P(\text{Recipe Source} \cap \text{Purchase})}{P(\text{Purchase})} = \frac{0.000}{0.029} \approx 0.0
$$

$$
P(\text{Yahoo} | \text{Purchase}) = \frac{P(\text{Yahoo} \cap \text{Purchase})}{P(\text{Purchase})} = \frac{0.013}{0.029} \approx 0.448
$$

Therefore, based on the contingency table above, it is most likely that visitors from MSN make a purchase at Amazon.com



```


```{hint}
Treat that customers make a purchase as a given.
```
