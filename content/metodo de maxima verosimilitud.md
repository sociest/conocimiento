---
title: Método de Máxima Verosimilitud
---
> Verosímil sinónimo de probable
Sea $X$ una v.a. poblacional con fdp $f(x,\theta)$. Se toma una m.a. de $X \{x_{1},x_{2},\dots,x_{n}\}$, luego la función de verosimilitud se define como $L=f(x_{1},x_{2},\dots,x_{n};\theta)= f(x_{1};\theta)f(x_{2};\theta)\dots f(x_{n};\theta)=\prod_{i=1}^{n}f(x_{i};\theta)$
La función máximo verosímil, logaritmo, derivada respecto a $\theta$, e igualado a cero.
$$
\begin{align}
\ln L=\ln \prod_{i=1}^{n}f(x_{i};\theta)=\prod_{i=1}^{n}\ln f(x_{i};\theta)   \\
\frac{\partial \ln L}{\partial \theta}=0 \implies \sum_{i=1}^{n} \frac{\partial \ln f(x_{i},\theta)}{\partial \theta}=0 \to \hat{\theta}=? 
\end{align}
$$