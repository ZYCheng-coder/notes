**三维刚体运动:**  
坐标系定义:  
世界坐标系W;  
IMU坐标系I;  
相机坐标系C;  

&emsp;

**四元数**  
* 旋转矩阵 $\mathbf{R}$ 使用四元数 $\mathbf{q}$ 描述  
* 四元数$\mathbf{q}$有一个实部和三个虚部,表示为$\mathbf{q}=[q_0,q_1,q_2,q_3]^T$ 或 $\mathbf{q}=[w,x,y,z]^T$,也可以表示为$\mathbf{q}=[s,\mathbf{v}]^T$,其中$s$为标量,$\mathbf{v}$为虚部的矢量.  
* 四元数之间的乘法运算:  
$\begin{align}
\textbf{q}_a\otimes\textbf{q}_b&=w_aw_b-x_ax_b-y_ay_b-z_az_b\notag \\
& +(w_ax_b+x_aw_b+y_az_b-z_ay_b)\mathbf{\textit{i}}\notag \\
& +(w_ay_b-x_az_b+y_aw_b+z_ax_b)\mathbf{\textit{j}}\notag \\
& +(w_az_b+x_ay_b-y_ax_b-z_aw_b)\mathbf{\textit{k}}\notag \\
\end{align}$
或
$$\begin{align}
\mathbf{q}_a\otimes\mathbf{q}_b=
\begin{bmatrix}s_as_b-\mathbf{v}_a^T\mathbf{v}_b&,& s_a\mathbf{v}_b+s_b\mathbf{v}_a+\mathbf{v}_a\times\mathbf{v}_b\end{bmatrix} \notag
\end{align}$$
* 四元数和角轴的转换关系:  
某个旋转运动的旋转轴为单位向量$\mathbf{u}$,绕该轴的旋转角度为$\theta$,对应的单位四元数为$q=\begin{bmatrix} \cos\frac{\theta}{2}\\ \mathbf{u}s\in\frac{\theta}{2} \end{bmatrix}$,当旋转为极小值时,$\Delta\mathbf{q}=\begin{bmatrix}\cos\frac{\delta\theta}{2}\\ \mathbf{u}\sin\frac{\delta\theta}{2}\end{bmatrix}\approx\begin{bmatrix}1\\\mathbf{u}\frac{\delta\theta}{2}\end{bmatrix}=\begin{bmatrix}1\\ \frac{1}{2}\mathbf{{\delta\theta}}\end{bmatrix}$,其中$\delta\mathbf{\theta}$的方向表示旋转轴,模长表示旋转角度.  

&emsp;

**对时间求导**
