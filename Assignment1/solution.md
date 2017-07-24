# 1 Softmax
For every ${x}_{i}$ in $\mathbf{x}$
$$
softmax{(\mathbf{x}+c)}_{i}=\frac{e^{{x}_{i}+c}}{\sum_{j}e^{{x}_{j}+c}}=\frac{e^{c}\cdot e^{{x}_{i}}}{e^{c}\cdot\sum_{j}e^{{x}_{j}}}=\frac{e^{{x}_{i}}}{\sum_{j}e^{{x}_{j}}}=softmax{(\mathbf{x})}_{i}
$$
so
$$
softmax{(\mathbf{x}+c)}=softmax{(\mathbf{x})}
$$

# 2 Neural Network Basics
(a)
$$
{\sigma}'(x)=-\frac{1}{{({1+{e}^{-x}})}^{2}}\cdot{({e}^{-x})}'=-\frac{-{e}^{-x}}{(1+{e}^{-x})^{2}}=\frac{1}{1+{e}^{-x}}\cdot\frac{{e}^{-x}}{1+{e}^{-x}}=\sigma(x)(1-\sigma(x))
$$

(b)
Assume ${y}_{k}=1$, then
$$
CE(\mathbf{y,\hat{y}})=-\log{(\hat{y}_{k})}=-\log{(softmax({\theta}_{k}))}=-\log\frac{{e}^{{\theta}_{k}}}{\sum_{i}{e}^{{\theta}_{i}}}
$$
so
$$
\frac{\partial CE}{\partial {\theta}_{j}}={\hat{y}_{k}}^{-1}\frac{{e}^{{\theta}_{k}}{e}^{{\theta}_{j}}}{{(\sum_{i}{e}^{{\theta}_{i}})}^{2}}={\hat{y}_{k}}^{-1}{\hat{y}_{k}}{\hat {y}_{j}}=\hat{y}_{j}(j\neq k)
$$
$$
\frac{\partial CE}{\partial {\theta}_{k}}={\hat{y}_{k}}^{-1}(\frac{{e}^{{\theta}_{k}}{e}^{{\theta}_{k}}}{{(\sum_{i}{e}^{{\theta}_{i}})}^{2}}-\frac{{e}^{{\theta}_{k}}}{\sum_{i}{e}^{{\theta}_{i}}})={\hat{y}_{k}}^{-1}({\hat{y}_{k}}^{2}-{\hat{y}_{k}})={\hat{y}_{k}}-1
$$
