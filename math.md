# 公式
$$
y_i \approx \beta_0 + \sum_{j=1}^m \beta_j \times x_j^i
$$

$$
y_i \approx \sum_{j=0}^m \beta_j \times x_j^i = \vec{\beta} \cdot \vec{x_i}
$$

$$
\vec{\hat{\beta}} = \underset{\vec{\beta}}{\text{arg min}} \, L(D, \vec{\beta}) = \underset{\vec{\beta}}{\text{arg min}} \sum_{i=1}^n \left( \vec{\beta} \cdot \vec{x_i} - y_i \right)^2
$$

$$
\begin{aligned}
L(D, \vec{\beta}) &= \| X\vec{\beta} - Y \|^2 \\
&= (X\vec{\beta} - Y)^\top (X\vec{\beta} - Y) \\
&= Y^\top Y - Y^\top X\vec{\beta} - \vec{\beta}^\top X^\top Y + \vec{\beta}^\top X^\top X \vec{\beta}
\end{aligned}
$$

$$
\begin{aligned}
\frac{\partial L(D, \vec{\beta})}{\partial \vec{\beta}} &= \frac{\partial}{\partial \vec{\beta}} \left( Y^\top Y - Y^\top X\vec{\beta} - \vec{\beta}^\top X^\top Y + \vec{\beta}^\top X^\top X \vec{\beta} \right) \\
&= -2 X^\top Y + 2 X^\top X \vec{\beta}
\end{aligned}
$$

$$
\begin{aligned}
-2 X^\top Y + 2 X^\top X \vec{\beta} &= 0 \\
\Rightarrow X^\top X \vec{\beta} &= X^\top Y \\
\Rightarrow \vec{\hat{\beta}} &= \left( X^\top X \right)^{-1} X^\top Y
\end{aligned}
$$