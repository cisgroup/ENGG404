# Introduction

## Contingency Table

```{admonition} Contingency Table
A contingency table shows counts of cases on one **categorical** variable
contingent on the value of another (for every combination of both variables).
Contingency tables are useful for calculating conditional probabilities, as they
contain all the ingredients necessary for the computation.
```

## Examples
We want to investigate which host sends more buyers to the internet shopping website Amazon.com. In order to answer this question, we must gather data on two (categorical) variables:

1. The host that identifies the originating site, which is either MSN, RecipeSource, or Yahoo.
2. A binary variable that indicates whether the visit results in a purchase.

The contingency table below shows data for web shoppers at Amazon.com. It
contains the following pieces of information:
- The website through which a customer ended up at Amazon.com
- Whether the customer made a purchase or not

```{list-table}
:header-rows: 1
:name: table-amazon-1

* -
  - MSN
  - Recipe Source
  - Yahoo
  - Total
* - No Purchase
  - 6.973
  - 4.282
  - 5.848
  - 17.103
* - Purchase
  - 285
  - 1
  - 230
  - 516
* - Total
  - 7.258
  - 4.283
  - 6.078
  - 17.619
```


The contingency table above shows counts (number of customers) and not probabilities. We can transform the counts into probabilities by dividing each number by the total (17.619 in this case). The table below shows the probabilities corresponding to the counts in the contingency table above.

```{list-table}
:header-rows: 1
:name: table-amazon-2

* -
  - MSN
  - Recipe Source
  - Yahoo
  - Total
* - No Purchase
  - 0.396
  - 0.243
  - 0.332
  - 0.971
* - Purchase
  - 0.016
  - 0.000
  - 0.013
  - 0.029
* - Total
  - 0.412
  - 0.243
  - 0.345
  - 1.0
```
