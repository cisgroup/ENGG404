# Applications

## Naive Bayes Classification

```{epigraph}
Naive Bayes is one of the most efficient and effective inductive learning algorithms for machine learning and data mining. Its competitive performance in classification is surprising, because the conditional independence assumption on which it is based, is rarely true in real-world applications.

-- Zhang, 2004
```

- Naive Bayes is useful for classification of emails whether they belong to the spam folder or are legitimate.
- Naive Bayes is useful for machine learning, (algorithms that can learn from data).
-  Naive Bayes is useful for clustering techniques, where all kinds of objects in the same group (called a cluster) are more similar (in some sense or another) to each other than to those in other groups (clusters).

```{admonition} Bayes’ Rule
Naive Bayes classification depends on Bayes’ Rule. For two events $A$ and $B$, Bayes’ rule can be expressed by the following relationship:

$$
P(B|A) = \frac{P(B \cap A)}{P(A)} = \frac{P(A \cap B)}{P(A)} = \frac{P(A|B)\cdot P(B)}{P(A)}
$$

provided that $P(A) \not= 0$.

Here, $P(B)$ is called the **a priori** probability of $B$ and $P(B|A)$ is called the **a posteriori** probability of $B$. Note that we expressed the probability of $B$ given $A$ in terms of $A$ given $B$.

```

```{attention}
**Conditional Independence Assumption**

Naive Bayes Classification relies heavily on two assumptions:
1. All events are equally important (they all have equal weights).
2. All events are mutually independent.

```

### Example: Weather Forecast

Let us assume the weather is as follows:

```{tabbed} Outlook
|          | yes |  no |
| -------- | --- | --- |
| Sunny    |  2  |  3  |
| Overcast |  4  |  0  |
| Rainy    |  3  |  2  |
```

```{tabbed} Temperature
|          | yes |  no |
| -------- | --- | --- |
| Hot      |  2  |  2  |
| Mild     |  4  |  2  |
| Cold     |  3  |  1  |
```

```{tabbed} Humidity
|          | yes |  no |
| -------- | --- | --- |
| High     |  3  |  4  |
| Normal   |  6  |  1  |
```

```{tabbed} Windy
|          | yes |  no |
| -------- | --- | --- |
| False    |  6  |  2  |
| True     |  3  |  3  |
```

```{tabbed} Play
| yes |  no |
| --- | --- |
|  9  |  5  |
```

Converting the counts into probabilities yields the table below. Note that the table above is not a contingency table!

```{tabbed} Outlook
|          | yes |  no |
| -------- | --- | --- |
| Sunny    |  $\frac{2}{9}$  |  $\frac{3}{5}$  |
| Overcast |  $\frac{4}{9}$  |  $\frac{0}{5}$  |
| Rainy    |  $\frac{3}{9}$  |  $\frac{2}{5}$  |
```

```{tabbed} Temperature
|          | yes |  no |
| -------- | --- | --- |
| Hot      |  $\frac{2}{9}$  |  $\frac{2}{5}$  |
| Mild     |  $\frac{4}{9}$  |  $\frac{2}{5}$  |
| Cold     |  $\frac{3}{9}$  |  $\frac{1}{5}$  |
```

```{tabbed} Humidity
|          | yes |  no |
| -------- | --- | --- |
| High     |  $\frac{3}{9}$  |  $\frac{4}{5}$  |
| Normal   |  $\frac{6}{9}$  |  $\frac{1}{5}$  |
```

```{tabbed} Windy
|          | yes |  no |
| -------- | --- | --- |
| False    |  $\frac{6}{9}$  |  $\frac{2}{5}$  |
| True     |  $\frac{3}{9}$  |  $\frac{3}{5}$  |
```

```{tabbed} Play
| yes |  no |
| --- | --- |
|  $\frac{9}{14}$  |  $\frac{5}{14}$  |
```

```{dropdown} **Question**: What is the probability that the outlook is sunny, the temperature is considered cold, the humidity is high and that it is windy and play is either ‘yes’ or ‘no’?


**Solution**: We get for a sunny outlook, a cool temperature, high humidity, windy weather and play equal to yes: $\frac{2}{9} \cdot \frac{3}{9}  \cdot \frac{3}{9} \cdot \frac{3}{9} \cdot \frac{9}{14} \approx 0.0053$.

We get for no sunny outlook, no cool temperature, no high humidity, no windy
weather and play equal to no: $\frac{3}{5} \cdot \frac{1}{5}  \cdot \frac{4}{5} \cdot \frac{3}{5} \cdot \frac{5}{14} \approx 0.0206$

So, transforming this to probabilities by normalizing the above values, we get:

- $P(\text{yes}) = \frac{0.0053}{0.0053+0.0206} = 0.205 = 20.5\%$
- $P(\text{no}) = \frac{0.0206}{0.0053+0.0206} = 0.795 = 79.5\%$

We can immediately see that these probabilities add up to 1.
```
