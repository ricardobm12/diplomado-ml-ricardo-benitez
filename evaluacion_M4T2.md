# Evaluación — Módulo 4 · Tema 2: GLM con Python

**Alumno:** Ricardo Antonio
**Variable asignada:** `nivel_bonus_cat`  (nivel bonus-malus)
**Fecha de entrega:** ________________

> **Instrucciones.** Este archivo evalúa las tres sesiones del tema. Las tablas ya vienen
> calculadas; tu trabajo es **responder las preguntas de interpretación** en el espacio
> "**Tu respuesta:**". Se evalúa la interpretación, no el código. Máx. 4–6 líneas por respuesta.
> Todas tus preguntas usan **tu variable asignada** (`nivel_bonus_cat`). Guarda y sube este archivo a tu repositorio.

---

## Parte 1 · Sesión 1 — Modelo de Frecuencia

**Diagnóstico del supuesto de Poisson (modelo completo):**

| métrica | valor |
| --- | --- |
| φ de Pearson | 1.1664 |
| Cameron-Trivedi α | 0.0744 |
| z | 15.80 |
| p-value | 3.7e-56 |

**Rating factors de frecuencia para `nivel_bonus_cat`** (base × RF reproduce la tasa empírica; diferencia máx = 4.7e-05):

| nivel | RF_frec | IC_inf | IC_sup | p | tasa_emp |
| --- | --- | --- | --- | --- | --- |
| (-1, 0] (ref) | 1 | 1 | 1 | 0 | 0.1006 |
| (0, 1] | 1.1569 | 1.1061 | 1.21 | 0 | 0.1163 |
| (1, 2] | 1.2736 | 1.1942 | 1.3583 | 0 | 0.1281 |
| (10, 25] | 2.6544 | 2.5358 | 2.7785 | 0 | 0.2669 |
| (2, 5] | 1.4953 | 1.4319 | 1.5614 | 0 | 0.1504 |
| (5, 10] | 1.9009 | 1.8284 | 1.9763 | 0 | 0.1912 |

**P1.** ¿Se cumple la equidispersión? Justifica con φ **y** con Cameron-Trivedi, y di qué familia usarías.
**Tu respuesta:**

**P2.** Interpreta los rating factors de tu variable: nivel más alto y más bajo, traducidos a % de
recargo/descuento. ¿Algún IC cruza 1 o tiene p > 0.05? ¿Qué harías con ese nivel?
**Tu respuesta:**

**P3.** ¿Por qué el GLM one-way reproduce exactamente la tasa empírica, y qué aporta el GLM que una
tabla empírica no puede dar?
**Tu respuesta:**

---

## Parte 2 · Sesión 2 — Severidad y Selección de Modelos

**Comparación de modelos de frecuencia:**

| modelo | AIC | BIC | pseudoR2_McF |
| --- | --- | --- | --- |
| Poisson | 125,081.7 | 125,261.7 | 0.0198 |
| Binomial Negativa | 124,925.7 | 125,105.8 | 0.021 |

**Rating factors de severidad (Gamma) para `nivel_bonus_cat`:**

| nivel | RF_sev | severidad_emp |
| --- | --- | --- |
| (-1, 0] (ref) | 1 | 1,191 |
| (0, 1] | 1.0957 | 1,305 |
| (1, 2] | 1.0862 | 1,293 |
| (10, 25] | 1.1708 | 1,394 |
| (2, 5] | 1.1185 | 1,332 |
| (5, 10] | 1.1695 | 1,392 |

**P4.** ¿Por qué se usa **Gamma** para severidad y no una regresión lineal sobre log(Y)? (menciona la
propiedad del CV y por qué Lognormal no es GLM).
**Tu respuesta:**

**P5.** Según la tabla de comparación, ¿qué modelo elegirías? Justifica con AIC/BIC. ¿Por qué el pseudo R²
es tan bajo y eso NO significa que el modelo sea malo?
**Tu respuesta:**

**P6.** Compara tus rating factors de frecuencia (Parte 1) con los de severidad para `nivel_bonus_cat`. ¿Apuntan en
la misma dirección? ¿Qué implica eso para separar Frecuencia × Severidad?
**Tu respuesta:**

---

## Parte 3 · Sesión 3 — Validación y Tarifa

**Validación out-of-sample del modelo de frecuencia:**

| metrica | valor | ideal |
| --- | --- | --- |
| Gini (test) | 0.2315 | > 0.30 aceptable |
| Ratio pred/obs (test) | 1.0249 | ≈ 1.00 |

**Prima pura por nivel de `nivel_bonus_cat`** (Frecuencia × Severidad, con su factor de tarifa):

| nivel | prima_pura_modelo | factor_tarifa |
| --- | --- | --- |
| (-1, 0] (ref) | 118.65 | 0.6507 |
| (0, 1] | 152.88 | 0.8385 |
| (1, 2] | 166.54 | 0.9134 |
| (10, 25] | 373.6 | 2.0489 |
| (2, 5] | 200.26 | 1.0983 |
| (5, 10] | 267.13 | 1.465 |

**P7.** Interpreta las métricas de validación: ¿el modelo está bien calibrado (ratio pred/obs)? ¿discrimina
bien el riesgo (Gini)? ¿Qué mide cada una?
**Tu respuesta:**

**P8.** Lee la tabla de tarifa: ¿qué nivel de tu variable paga la prima pura más alta y cuál la más baja?
Traduce el factor de tarifa a un recargo/descuento sobre la prima promedio.
**Tu respuesta:**

**P9. (Conclusión de nota técnica).** En 3–4 líneas, redacta cómo `nivel_bonus_cat` afecta la tarifa, integrando
frecuencia, severidad y prima pura, en estilo defendible ante la CNSF.
**Tu respuesta:**

---
*Evaluación generada automáticamente · Diplomado ML en Seguros · FC UNAM · Módulo 4 · Tema 2*
