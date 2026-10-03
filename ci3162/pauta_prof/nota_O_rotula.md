# ¿Qué es el $O$ en la ecuación de torque?

Sí, exactamente — **$O$ es la profundidad de la rótula** bajo la superficie libre (del estanque que estés analizando). No es una variable "nueva": es el mismo truco de siempre, escrito de una forma compacta.

## De dónde sale, conectándolo con $y_R$

Ya vimos que

$$y_R = y_G + \frac{I_{xG}}{S\,y_G}$$

te da la profundidad del **centro de presión**, medida desde la **superficie libre** — no desde la rótula. Pero lo que realmente quieres para el torque es el **brazo de palanca respecto de la rótula**, que es la distancia entre el centro de presión y la rótula:

$$\text{brazo} = y_R - O$$

donde $O$ es, precisamente, la profundidad de la rótula (para que la resta te dé la distancia entre ambos puntos, medida a lo largo de la misma línea).

El torque respecto de la rótula es entonces $F\cdot(y_R-O)$. Si lo desarrollas usando $F=\rho g\,y_G\,S$ y la fórmula de $y_R$:

$$T = F(y_R - O) = \rho g\, y_G S\left[y_G + \frac{I_{xG}}{S y_G} - O\right] = \rho g\, y_G S (y_G - O) + \rho g\, I_{xG}$$

$$\boxed{T = \rho g \Big[ I_{xG} + y_G (y_G - O)\, S \Big]}$$

Esa es exactamente la fórmula que usó el profesor (con $x_G$ en vez de $y_G$, mismo significado) — no calculó $y_R$ por separado y después restó $O$; sustituyó $O$ directo dentro de la expansión algebraica, pero es matemáticamente lo mismo que hicimos en la Clase Auxiliar para el brazo $b_a = y_{R1} - H_1/\sin\theta$ (ahí $H_1/\sin\theta$ jugaba el rol de $O$).

## El valor concreto en P7

En ese problema, $O = h_1 - R$ porque la rótula está a una altura $R$ sobre el piso, y el piso está a profundidad $h_1$ bajo la superficie del estanque 1 — entonces la rótula queda a profundidad $(h_1 - R)$.

## Por qué importa que aparezca explícitamente

Cuando la rótula **coincide** con el centroide de la franja que estás analizando (como pasó con el estanque 2, donde $x_G = O = h_2 - R$), el término $y_G(y_G - O)$ se anula solo — por eso ahí sobrevivió únicamente el término $I_{xG}$. Cuando la rótula **no** coincide con el centroide (como con el estanque 1), ese término no se cancela y aporta al torque. Es la misma idea de "¿dónde está la rótula respecto del centroide?" que ya vimos en la compuerta plana y en la semicilíndrica — aquí solo está escrita de forma más compacta, metiendo la resta dentro de la fórmula en vez de calcularla aparte.
