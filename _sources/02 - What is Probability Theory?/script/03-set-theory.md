# Set Theory
## Introduction

For simple probability calculations, it is useful to know just a little set theory.  Therefore we cover in this section a few basic definitions. This part may be boring, but please stay with us. Below are a few definitions for arbitrary sets $A$ and $B$.

## Set Theory: Definitions

```{admonition} Union
The union of two events $A$ and $B$ is the set that contains all the events that are either in $A$ or in $B$ or in both sets.

Notation: $A \cup B$.
```

```{admonition} Intersection
The intersection of two events $A$ and $B$ is the set that contains all the
events that are both in $A$ and in $B$.

Notation: $A \cap B$.
```

```{admonition} Complement
The complement of an event $A$ with respect to an event $B$ refers to all
elements that are in $B$, but not in $A$. This is usually denoted by $B \cap A^c$
or $B \setminus A$.
```

```{admonition} Mutually Exclusive
Two events $A$ and $B$ are said to be mutually exclusive if they have no basic outcomes in common. This is usually denoted by $B \cap A = \emptyset$.
```

```{admonition} Collectively Exhaustive
Events $A_1, A_2, \dots, A_n$ are said to be collectively exhaustive events if
$A_1 \cup A_2 \dots \cup A_n = S$, i.e. the events in union completely cover the
sample space $S$.
```

```{image} images/venn.png
:height: 500px
:name: image-venn
```

## Examples

In this example, we throw a six-sided die. Let $A$ be the event that the outcome is either 1, 2 or 3. Let $B$ be the event that the outcome is an even number, so either 2, 4 or 6.

```{dropdown} **Question 1**: Determine the union of $A$ and $B$, i.e. $A \cup B$.

**Solution**: $A \cup B = \{1,2,3,4,6\}$, as these are the numbers that are either in $A$ or in $B$.
```


```{dropdown} **Question 2**: Determine the intersection of $A$ and $B$, i.e. $A \cap B$.

**Solution**: $A \cap B = \{2\}$, as this is the only number that is both in $A$ and in $B$ or both.
```


```{dropdown} **Question 3**: Determine the completement of $A$, i.e. $A^c$.

**Solution**: $A^c = \{4,5,6\}$, as these are all the numbers in $S$ that are not in $A$.
```

```{dropdown} **Question 3**: Determine the completement of $B$, i.e. $B^c$.

**Solution**: $B^c = \{1,3,5\}$, as these are all the numbers in $S$ that are not in $B$.
```
