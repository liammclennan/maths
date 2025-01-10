# Bayesian Inference

## Pre-requisite Knowledge

$P(X,Y|W,Z)$ means the probability of $X$ and $Y$, given $W$ and $Z$.

$P(X,Y) = P(X) * P(Y)$

$P(X)$ or $P(Y)$ = $P(X) + P(Y) - P(X,Y)$

## Bayes' Theorem

Used to reverse conditional probability.

$P(A|B) = \frac{P(B|A)P(A)}{P(B)}$

$P(belief|data)$ is called **posterior probability**.

<img width="571" alt="image" src="https://github.com/user-attachments/assets/f39d3034-a91e-4e83-8f94-1840f49435c5" />

$let D = data, H = belief$ 

then $P(H|D) = \frac{P(D|H)P(H)}{P(D)}$

Event without a way to find $P(D)$ we can still use Bayes theorem to compare the unnormalized posteriors for different hypotheses. $\frac{P(H_1|D)}{P(H_2|D)}$ is how many time more likely is $H_1$ than $H_2$.

## Parameters

A *parameter* is some unknown value of a sample. 
