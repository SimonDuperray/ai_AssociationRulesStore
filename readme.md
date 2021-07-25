# Association Rules Learning - Apriori Model

The Apriori model imposes 3 crucial criteria for the evaluation of the rules's quality:

<ul>
   <li>Support</li>
   <li>Confidence</li>
   <li>Lift</li>
</ul>

## Support

```
Support({X}->{Y}) = (Transactions containing both X and Y)/(Total number of transactions)
```
idea: how frequent an itemset is in all the transactions

## Confidence

```
Confidence({X}->{Y}) = (Transactions containing both X and Y)/(Transactions containing X)
```
idea: likeliness of occurrence of consequent on the cart given the cart already has the antecedents

## Lift

```
Lift({X}->{Y}) = [(Transactions containing both X and Y)/(Transactions containing Y)]/(Fraction of transactions containing Y)
```
idea: controls the support of consequent while calculating the conditional probability of occurence of {Y} given {X}

## Bilan

The rule we obtained with the higher confidence is: (tomato sauce-ground beef):

```
|      lhs     |     rhs     |  support  | confidence |  lift  |
|--------------|-------------|-----------|------------|--------|
| tomato sauce | ground beef | 0.005333  |  0.377358  |3.840659|
```

So, if one customer bought tomtato sauce, there is 37% chance that he also bought ground beef.