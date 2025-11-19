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

## 牛顿法
$F(x + \Delta x) \approx F(x) + \frac{\partial F}{\partial x} \Delta x = 0$

# simulate
## PBD
![](../assets/private/pbd_1.png)
![](../assets/private/pbd_2.png)
![](../assets/private/pbd_3.png)
$C(p_1, p_2) = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2 + (z_1 - z_2)^2} - d = |p_1 - p_2| - d$
$\nabla_{p_1} C = (\frac{\partial C}{\partial x_1}, \frac{\partial C}{\partial y_1}, \frac{\partial C}{\partial z_1})$
$\frac{\partial C}{\partial x_1} = \frac{x_1 - x_2}{|p_1 - p_2|}$
$\nabla_{p_1} C = \frac{1}{|p_1 - p_2|}(x_1 - x_2, y_1 - y_2, z_1 - z_2) = \frac{p_1 - p_2}{|p_1 - p_2|}$
![](../assets/private/pbd_4.png)
![](../assets/private/pbd_5.png)

## XPBD
![](../assets/private/xpbd_1.png)
一阶泰勒展开
![](../assets/private/xpbd_2.png)
![](../assets/private/xpbd_3.png)
第一行结果
![](../assets/private/xpbd_4.png)
代入第二行
![](../assets/private/xpbd_5.png)
![](../assets/private/xpbd_6.png)

## VBD