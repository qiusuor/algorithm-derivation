逻辑回归

数据：$(X,Y),X \in R^n, Y \in \{0,1\}$

模型：$P_1=P(y_i=1|x_i)=\frac{1}{1+e^{-Wx_i}} \\ P_0=P(y_i=0|x_i)=\frac{e^{-Wx_i}}{1+e^{-Wx_i}} \\ P(y_i|x_i)=P_1^{y_i}P_0^{1-y_i}$

MLE求解：


$$
\begin{align}

\hat w &= \arg\max \limits_w  logP(Y|X) \\

&=  \arg\max \limits_w log \prod P(y_i|x_i) \\

&=  \arg\max \limits_w \sum log P(y_i|x_i) \\

&=  \arg\max \limits_w \sum log P_1^{y_i}P_0^{1-y_i} \\

&=  \arg\max \limits_w \sum (y_ilog P_1+(1-y_i)P_0) \\

\end{align}
$$

得到交叉熵损失：

$loss=-\sum (y_ilog P_1+(1-y_i)P_0) $

