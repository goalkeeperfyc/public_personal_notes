# Assumption for Generalized Linear Model
- Dropping normality
- Dropping constant variance
- Assuming a function of E(Y) linear in parameters, not E(Y) itself
$$
g(E(Y)) = \beta_0 + \beta_1X_1 + ... + \beta_nX_n
$$
---

- logistic regression is $log(odds)$.
- $odds = \frac{p}{1-p}$
- The change of odds ratio is $\exp(\beta)$
- The probability is $\frac{odds}{odds+1}$

The odds ratio is defined as the ratio of the odds of A in the presence of B and the odds of A in the absence of B.

$$
odds\_ratio = \frac{odds(B|A = 1)}{odds(B|A = 0)}
$$

In logistic regression

$$
odds\_ratio = \frac{odds(y = 1|x_1)}{odds(y = 1|x_2)}
$$

$x_1, x_2$ are different conditions. $y=1$ corresponses to A in the above formula.

# Interpret $\beta$
The meaning of coefficient $\beta_1$: With other variables unchanged, $x_1$ increases one unit, the odds of $y=1$ increases by $exp(\beta_1) - 1$ times.

$e^0 = 1$, which means as long as $\beta_1 > 0$, $e^{beta_1} > 1$. Thus the increasing of $x_1$ will increase the odds of $y=1$, as long as increasing the possibility of $y=1$.

# odds, odds ratio and possibility
$$
p = \frac{\#(y = 1)}{\#y}
$$

$$
odds = \frac{p}{1-p} 
$$

$$
p = \frac{odds}{odds+1}
$$

$$
odds\_ratio = \frac{odds(y = 1|x_1)}{odds(y = 1|x_2)}
$$

- $exp(\beta_1)$ is the change of odds ratio.
- $\beta_1$ can not only tell us wheher the odds increase or not, but also how much the increasing or decreasing is. ($exp(x_1) - 1$ times)
- $\beta_1$ can only tell us whether the possibility increase or not. If we want to know how much it is, we need to know all variables values before and after the change.