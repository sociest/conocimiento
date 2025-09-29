---
tags:
  - definicion
title: Estimador
draft: false
---
> [!info] [[definicion|Definición]]
> Un [[estadistico | estadístico]] es cualquier función $T$ de los datos muestrales $(X_1,X_2,\cdots,X_n)$ que no depende de parámetros desconocidos:
> $T = T(X_1,X_2,\cdots,X_n)$.

> [!quote] Contexto
> Es la unidad básica de la estadística inferencial: resumir datos para estimar parámetros poblacionales o describir características de la muestra.

> [!example] [[ejemplo|Ejemplo]]
> - La **media muestral** $\bar X = \tfrac1n\sum_i X_i$es un estadístico.  
> - El **número de valores superiores a 10** en la muestra, $\sum_i \mathbf{1}_{\{X_i>10\}}$​, también lo es.

## Suficiencia
Si $\hat{\theta}$ del parámetro $\theta$ emplea efectivamente la información de una m.a. de tamaño $n$ decimos que es un estimador suficiente, tal que cumple.
$$
\begin{align}
\text{Condicion de suficiencia}  \\
f(x_{1},x_{2},\dots,x_{n};\theta)=g(\hat{\theta};\theta)h(x_{1},x_{2},\dots,x_{n}) \\
\text{Donde} \begin{cases}
f(x_{1},x_{2},\dots x_{n};\theta)=\prod_{i=1}^{n}f(x_{i};\theta) \quad\text{por ser una m.a.} \\
g(\hat{\theta};\theta): \text{Funcion que depende de } \hat{\theta},\theta \\
h(x_{1},x_{2},\dots,x_{n}): \text{Funcion que solo depende de la m.a.}
\end{cases}
\end{align}
$$

### Ejemplos
Sea $\bar{X}$ La media muestral verificar que es un estimador suficiente.

Sea $X$ una v.a. poblacional con distribución normal con media $\mu_{x}$ (Desconocida) y $\sigma_{X}^{2}$ (Conocida).
Sol. $$
\begin{align}
x \to N(\mu_{x},\sigma_{o}^{2}) \quad E(\bar{X})=\mu_{x} \quad \text{Insesgado} \\
f(x;\theta=\mu_{x})=\frac{1}{\sqrt{ 2 \pi }\sigma_{o}}e^{- \frac{1}{2}\left( \frac{x-\mu_{x}}{\sigma_{o}} \right)^{2}}\quad-\infty<x<\infty \\
\text{m.a: }X_{1},X_{2},\dots,X_{n} \\
f(x_{1},x_{2},\dots,x_{n};\mu_{x})=\prod_{i=1}^{n}{f(x_{i};\mu_{x})}=\prod_{i=1}^{n}{\frac{1}{\sqrt{ 2 \pi }\sigma_{o}}e^{- \frac{1}{2}\left( \frac{x_{i}-\mu_{x}}{\sigma_{o}} \right)^{2}}} \\
=\frac{1}{(\sqrt{ 2 \pi }\sigma_{o})^{2}}e^{- \frac{1}{2} \sum_{i=1}^{n}{ \left( \frac{x_{i}-\mu_{x}}{\sigma_{o}} \right)^{2}}} \\
\text{primero} \sum_{i=i}^{n}{(X_{i}-\mu_{x})^{2}}=\sum_{i=1}^{n}{[(x_{i}-\bar{x})-(\mu_{x}-\bar{x})]^{2}}=\sum_{i=1}^{n}{[(x_{i}-\bar{x})^{2}-2(\mu_{x}-\bar{x})(x_{i}-\bar{x})+(\mu_{x}-\bar{x})^{2}]} \\
=\sum_{i=1}^{n} (x_{i}-\bar{x})^{2}-2(\mu_{x}-\bar{x})\sum_{i=1}^{n}(x_{i}-\bar{x})+n(\mu_{x}-\bar{x})^{2}=\sum_{i=1}^{n}(X_{i}-\bar{x})^{2}+n(\mu_{x}-\bar{x})^{2} \\
\text{aplicando en la original} \\
=ke^{-1/2 \left[ n(\mu_{x}-\bar{x})^{2}+\sum_{i=1}^{n}(X_{i}-\bar{x})^{2} \right]}=ke^{-\frac{n}{2\sigma_{o}^{2}}(\mu_{x}-\bar{x})^{2}}e^{-\frac{1}{2\sigma_{o}^{2}}\sum_{i=1}^{n}(x_{i}-\bar{x})^{2} } \\
\text{Que es de la forma } ke^{g(\bar{x};\mu_{x})}e^{h(x_{1},x_{2},\dots,x_{n})}
\end{align}
$$