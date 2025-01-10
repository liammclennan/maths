Probability
=====

An `outcome` is a result of an `experiment`. The `sample space (S)` is the set of all possible outcomes. An `event` is a subset of the `sample space (S)`.

If all outcomes of an experiment are equally likely then:

    P(E) = n(E) / n(S)

i.e. the probability of event `E` is the # of outcomes that belong to the event divided by the total number of outcomes. E.g. E = heads and I toss a coin then `P(E) = 1/2`.

The complement of an event `A` is the rest of the sample space:

$\bar{A} = S - A$

$P(\bar{A}) = 1 - P(A)$

$P(A) + P(\bar{A}) = P(S) = 1$

i.e. The event `A` or its compliment must always happen. So it has the same probability as the sample space, which is `1`.

### Probability of combined events

    P(A ∪ B) = P(A) + P(B) - P(A ∩ B)

### Conditional Probability

Probability of B, given A:

    P(B|A)

#### Conditional probability rule

    P(B|A) = P(A ∩ B) / P(A)

### Addition rule for disjoint events

For **disjoint** events.

    P(A or B) = P(A) + P(B)

#### Product Rule

For independent events `P(B|A) = P(B)` so the conditional probability rule becomes `P(B|A) = P(A ∩ B) / P(A)` or `P(A ∩ B) = P(B|A) * P(A)`

When `A` and `B` are independent then `P(A|B) = P(A)` and `P(B|A) = P(B)` so the product rule becomes

    P(A ∩ B) = P(A) * P(B)

### Expected # of Occurances

    = n * P(E)

Where n = # of experiments.

### Probability Tree

Shows all possible outcomes of an experiment. The first branches have marginal probabilities. Subsequent branches have conditional probabilities. The probabilities of the leaf nodes sum to `1`.

## Probability Density Function

Function that gives a probability as a distribution. Area under the curve must equal 1. Used to find the probability of a probability being in a particular range by integrating that part of the function. 

## Cumulative Density Function

Gives the probability that 

<script>
</script>
