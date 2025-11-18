# 计组

# CPP

# 数学

## 外积
$A = (x_1, y_1, z_1), B = (x_2, y_2, z_2)$
$A \times B = (y_1 z_2 - z_1 y_2, z_1 x_2 - x_1 z_2, x_1 y_2 - y_1 x_2)$

## 克拉莫法则
$A x = b$
$A = (a_1, a_2, a_3), A_1 = (b, a_2, a_3), ...$
$x_i = \frac{det(A_i)}{det(A)}$

## 四元数
$q_1 = (w_1, \vec{v_1}), q_2 = (w_2, \vec{v_2}), p = q_1 q_2$
$p.w = w_1 w_2 - \vec{v_1} \cdot \vec{v_2}$
$p.v = w_1 \vec{v_2} + w_2 \vec{v_1} + \vec{v_1} \times \vec{v_2}$

# simulate
## PBD
```python
x_old = x
for _ in range(JacobiIters):
    for i in range(len(vertex)):
        x_tmp[i] = 0
        n[i] = 0
    for e in range(len(edges)):
        i = e[0]
        j = e[1]
        x_ij = x[i] - x[j]
        x_tmp[i] += x[i] - 0.5 * (x_ij.len() - L[e]) * (x_ij / x_ij.len())
        x_tmp[j] += x[i] + 0.5 * (x_ij.len() - L[e]) * (x_ij / x_ij.len())

for i in range(len(vertex)):
    v[i] += (x[i] - x_old[i]) / delta_t
```

## XPBD