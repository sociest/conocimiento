---
title: Error Cuadrático Medio
tags:
  - definicion
---
Sea $\hat{\theta}=g(X_{1},X_{2},\dots,X_{n})$ un estimador de $\theta$. El error cuadrático medio de $\hat{\theta}$ se define como
$$
ECM(\hat{\theta})=E(\hat{\theta}-\theta)^{2}=V(\hat{\theta})+[\theta-E(\hat{\theta})]^{2}
$$El término $\theta-E(\hat{\theta})$ es el sesgo del estimador $\hat{\theta}$ y puede ser positivo o negativo o cero. El $ECM(\hat{\theta})$ es la suma de dos términos no negativos.

Entonces si $\hat{\theta}$ es un estimador insesgado de $\theta$ esto implica que
$$
ECM(\hat{\theta})=V(\hat{\theta})
$$
Verificando
$$
\begin{align}
ECM(\hat{\theta})=E(\hat{\theta}-\theta)^{2}=E([\hat{\theta}-E(\hat{\theta})]-[\theta-E(\hat{\theta})])^{2} \\
=E{[\hat{\theta}-E(\hat{\theta})]^{2}}-2[\theta-E(\hat{\theta})]E[\hat{\theta}-E(\hat{\theta})]+E{(\theta-E(\hat{\theta)})^{2}} \\
=V(\hat{\theta})+[\theta-E(\hat{\theta})]^{2}
\end{align}
$$