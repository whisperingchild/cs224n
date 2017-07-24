# 1 Softmax
For every ${x}_{i}$ in $\mathbf{x}$
$$
softmax{(\mathbf{x}+c)}_{i}=\frac{e^{{x}_{i}+c}}{\sum_{j}e^{{x}_{j}+c}}=\frac{e^{c}\cdot e^{{x}_{i}}}{e^{c}\cdot\sum_{j}e^{{x}_{j}}}=\frac{e^{{x}_{i}}}{\sum_{j}e^{{x}_{j}}}=softmax{(\mathbf{x})}_{i}
$$
so
$$
softmax{(\mathbf{x}+c)}=softmax{(\mathbf{x})}
$$
