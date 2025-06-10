---
title: Etiquetas
draft: true
---

## 5. Definición de Esperanza Matemática

> **Título:** Esperanza (Valor Esperado)  
> **ID:** `concepto-esperanza`  
> **Definición:** Para una variable aleatoria discreta XX,
> 
> E[X]=∑xx P(X=x).E[X] = \sum_{x} x \, P(X = x).
> 
> Para continua,
> 
> E[X]=∫−∞∞x fX(x) dx.E[X] = \int_{-\infty}^{\infty} x \, f_X(x)\,dx.
> 
> **Contexto:** Mide el “centro de gravedad” de la distribución.  
> **Ejemplo:** Si XX es el número de caras al lanzar dos monedas,
> 
> E[X]=0⋅14+1⋅12+2⋅14=1.E[X] = 0\cdot\tfrac14 + 1\cdot\tfrac12 + 2\cdot\tfrac14 = 1.
> 
> **Enlaces:**
> 
> - ← `concepto-var-aleat`
>     
> - → `concepto-varianza`
>     

---

## 6. Definición de Varianza

> **Título:** Varianza  
> **ID:** `concepto-varianza`  
> **Definición:**
> 
> Var(X)=E[(X−E[X])2]=E[X2]−(E[X])2.\mathrm{Var}(X) = E\bigl[(X - E[X])^2\bigr] = E[X^2] - (E[X])^2.
> 
> **Contexto:** Cuantifica la dispersión en torno a la esperanza.  
> **Ejemplo:** Para el dado justo, E[X]=3.5E[X]=3.5 y
> 
> E[X2]=12+22+⋯+626=916,Var(X)=916−(3.5)2=3512.E[X^2] = \tfrac{1^2+2^2+\dots+6^2}{6} = \tfrac{91}{6},\quad \mathrm{Var}(X) = \tfrac{91}{6} - (3.5)^2 = \tfrac{35}{12}.
> 
> **Enlaces:**
> 
> - ← `concepto-esperanza`
>     