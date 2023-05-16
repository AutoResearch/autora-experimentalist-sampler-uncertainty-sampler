# Uncertainty Sampler

The uncertainty sampler identifies experimental conditions $\vec{x}' \in X'$ with respect model uncertainty. Within the uncertainty sampler, there are three methods to determine uncertainty:

## Least Confident
$$
x^* = \operatorname{argmax} \left( 1-P(\hat{y}|x) \right),
$$

where $\hat{y} = \operatorname{argmax} P(y_i|x)$

## Margin

$$
x^* = \operatorname{argmax} \left( P(\hat{y}_1|x) - P(\hat{y}_2|x) \right),
$$

where $\hat{y}_1$ and $\hat{y}_2$ are the first and second most probable class labels under the model, respectively.

## Entropy
$$ 
x^* = \operatorname{argmax} \left( - \sum P(y_i|x)\operatorname{log} P(y_i|x) \right)
$$