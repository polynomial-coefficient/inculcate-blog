# 证明微分乘法律 $ d(\lambda \mu)=\lambda d\mu + \mu d\lambda $

<hr>

对微分乘法法则的推导,即证明: $\quad d(\lambda \mu)=\lambda d\mu + \mu d\lambda $
$$\\ \\$$

$$ 若 y=\mu \lambda ,\quad \lambda = f(x),\quad \mu = g(x), 二者均以 x 为自变量$$
$$\\ \\$$
$$y+\Delta y=(\mu +\Delta \mu) (\lambda +\Delta \lambda )$$
$$\\ \\$$
$$=\mu \lambda +\lambda \Delta \mu +\mu \Delta \lambda +\Delta \lambda \Delta \mu $$
$$\\ \\$$
$$y+\Delta y=y+\lambda \Delta \mu +\mu \Delta \lambda +\Delta \lambda \Delta \mu $$
$$\\ \\$$
$$\Delta y=\lambda \Delta \mu +\mu \Delta \lambda +\Delta \lambda \Delta \mu $$
$$\\ \\$$

$$
同时除以 \Delta x: \quad
\frac{\Delta y}{\Delta x}=\frac{\lambda \Delta \mu}{\Delta x}
+\frac{\mu \Delta \lambda }{\Delta x}
+\frac{\Delta \lambda \Delta \mu}{\Delta x}
$$

$$\\ \\$$

$$
引入极限,设 \Delta x \to 0: \\
\lim_{\Delta x \to 0}\frac{\Delta y}{\Delta x}=
\lambda \lim_{\Delta x \to 0} \frac{\Delta \mu}{\Delta x}

+\mu \lim_{\Delta x \to 0} \frac{\Delta \lambda }{\Delta x}

+\lim_{\Delta x \to 0} \frac{\Delta \lambda \Delta \mu}{\Delta x}
$$

$$\\ \\$$

$$
\lim_{\Delta x \to 0} \frac{\Delta \lambda \Delta \mu}{\Delta x}
= \lim_{\Delta x \to 0} \frac{\Delta \lambda}{\Delta x} \cdot
\lim_{\Delta x \to 0} \Delta \mu
$$

$$\\ \\$$
$$而\lim_{\Delta x \to 0} \Delta \mu =\lim_{\Delta x \to 0} g(x+\Delta x)-g(x)$$
$$\\ \\$$

$$
\because \Delta x \to 0,\quad
\therefore \lim_{\Delta x \to 0} \Delta \mu =0
$$

$$\\ \\$$

$$
得: \quad \frac{dy}{dx}= \lambda \frac{d\mu }{dx}
+\mu\frac{d\lambda }{dx} +\frac{d\lambda }{dx} \cdot 0
$$

$$\\ \\$$
$$\frac{dy}{dx}= \frac{\lambda d\mu +\mu d\lambda }{dx}$$
$$\\ \\$$
$$约去dx: \quad  dy=\lambda d\mu + \mu d\lambda $$
$$\\ \\$$
$$证明成立$$
