# 1. Bonferroni method

Let $\alpha_1, \dots, \alpha_m$ - hypothesis significance levels of $H_1, \dots, H_m$.

Thus, new significance levels will be: $\alpha_1^*, \dots, \alpha_m^* = \frac{\alpha}{m}$

# 2.Holm Method

Variation series of significance levels: $$p_{(1)} \leq \dots \leq p_{(m)}$$

If $p_{(1)}\geq \alpha_1,$ then accept all $H_0$, otherwise continue

New significance levels will be: $\alpha_1^* = \frac{\alpha}{m}, \alpha_2^* = \frac{\alpha}{m-1}, \dots, \alpha_i^* = \frac{\alpha}{m-i+1}, \alpha_m^* = \alpha$, where $\alpha_1^*, \dots, \alpha_i^*$ is significance levels of variation series. (they are sorted in in ascending order).

$p_i^*=\min(1, \max((m-i+1)p_i), p_{i-1}^*)$

```python
from statsmodels.sandbox.stats.multicomp import multipletests 

multipletests(data, alpha = 0.05, method = 'holm') 
```

#3. benjamini–hochberg method

Variation series of significance levels: $$p_{(1)} \leq \dots \leq p_{(m)}$$

If $p_{(m)}\leq \alpha_m,$ then reject all $H_0$, otherwise continue

New significance levels will be: $\alpha_1^* = \frac{\alpha}{m}, \alpha_2^* = \frac{\alpha}{m-1}, \dots, \alpha_i^* = \frac{\alpha}{m-i+1}, \alpha_m^* = \alpha$, where $\alpha_1^*, \dots, \alpha_i^*$ is significance levels of variation series. (they are sorted in in ascending order).

$p_i^*=\min(1, \frac{mp(i)}{i}, p_{i+1}^*)$

```python
from statsmodels.sandbox.stats.multicomp import multipletests 

multipletests(data, alpha = 0.05, method = 'fdr_bh') 
```



