# Retroalimentación — Ricardo Benítez
**Repo:** https://github.com/ricardobm12/diplomado-ml-ricardo-benitez
**Fecha de evaluación:** 2026-05-12
**Calificación final:** 9.55 / 10

## Resumen general
Excelente entrega.

## Desglose por sesión

### Sesión 1 — Instalación y configuración de Python — 1/1 pt
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\Sesion1\sesion1_M1_notebook.ipynb`. 33 de 36 celdas de código con contenido ejecutable.

### Sesión 2 — Tipos de datos básicos — 1/1 pt
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\Sesion2\sesion2_M1_notebook.ipynb`. 29 de 31 celdas de código con contenido ejecutable.

### Sesión 3 — Estructuras de datos + control de flujo — 1/1 pt
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\sesion3\sesion3_M1_notebook_Ricardo.ipynb`. 35 de 35 celdas de código con contenido ejecutable.

### Sesión 4 — Funciones — 1/1 pt
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\sesion4\sesion4_M1_notebook_Ricardo.ipynb`. 21 de 22 celdas de código con contenido ejecutable.

### Sesión 5 — Módulos / funciones avanzadas — 2.00/2 pts
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\sesion5\sesion5_M1_notebook_Ricardo.ipynb`.
- Notebook ejecutable: **0.5/0.5**
- Ejercicios completos: **0.5/0.5**
- Resultados correctos: **1.0/1.0**
- Las 3 tareas integradoras tienen código.
- Notebook ejecuta end-to-end sin errores.

### Sesión 6 — Módulos propios + inicio de Pandas — 1.67/2 pts
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\sesion6\sesion6_M1_notebook_Ricardo.ipynb`.
- Notebook ejecutable: **0.5/0.5**
- Ejercicios completos: **0.5/0.5**
- Resultados correctos: **0.67/1.0**  _(re-evaluado con comparación numérica estricta contra canónico)_
  - Tarea 1: ◐ parcial (11/20 números coinciden con el canónico)
  - Tarea 2: ✓ correcta (25/25 números coinciden)
  - Tarea 3: ◐ parcial (9/14 números coinciden con el canónico)

### Sesión 7 — Pandas avanzado — 1.88/2 pts
Archivo: `diplomado-ml-ricardo-benitez\Modulo1\sesion7\sesion7_M1_notebook_Ricardo.ipynb`.
- Notebook ejecutable: **0.5/0.5**
- Ejercicios completos: **0.5/0.5**
- Resultados correctos: **0.88/1.0**  _(re-evaluado con comparación numérica estricta contra canónico)_
  - Tarea 1: ✓ correcta (15/15 números coinciden)
  - Tarea 2: ✓ correcta (18/18 números coinciden)
  - Tarea 3: ✓ correcta (30/30 números coinciden)
  - Tarea 4: ◐ parcial (10/15 números coinciden con el canónico)


## Parte 2 — Sesiones 8 y 11

### Sesión 8 — Pipeline Completo — 1.56/2 pts
*(solo se evaluó el Ejercicio Integrador Final)*
- Corre hasta el Integrador: 0.50/0.5
- Integrador Final, 5 fases: 1.06/1.5
  - FASE 1: 0.90*0.3 = 0.27 (mayoria de numeros coinciden (40%))
  - FASE 2: 0.80*0.3 = 0.24 (coinciden algunos numeros clave (20%))
  - FASE 3: 0.40*0.3 = 0.12 (codigo corto sin numeros coincidentes)
  - FASE 4: 0.80*0.3 = 0.24 (coinciden algunos numeros clave (22%))
  - FASE 5: 0.65*0.3 = 0.20 (pocas coincidencias numericas (11%); codigo sustantivo y ejecuta)

### Sesión 11 — Práctica Final — 5.66/8 pts
*(solo se evaluó el Ejercicio Integrador Final "Mini Pricing Actuarial")*
- Corre hasta el Integrador: 0.50/1.0
  - Errores en celdas antes del integrador: [29]
  - FASE 1: 0.70*1.75 = 1.22 (codigo extenso (17 lineas) ejecuta; printeos no coinciden con canonico)
  - FASE 2: 0.55*1.75 = 0.96 (codigo presente ejecuta sin error; numeros no coinciden con canonico)
  - FASE 3: 1.00*1.75 = 1.75 (numeros coinciden (55% de canon cubierto))
  - FASE 4: 0.70*1.75 = 1.22 (codigo extenso (50 lineas) ejecuta; printeos no coinciden con canonico)

## Bonus — Sesiones 9 y 10
- S9 entregada correctamente: **Sí** (integrador correcto (100% de numeros coinciden))
- S10 entregada correctamente: **Sí** (mpl_ok=True sb_ok=True)
- Bonus aplicado: **+0.5**

## Calificación final
- Parte 1: 9.55 / 10
- Parte 2: 7.22 / 10
- Promedio: 8.385 / 10
- Bonus: +0.5
- **Final: 8.88 / 10**

---

# Retroalimentación — Módulo 4 · Tema 2 (GLM con Python)

**Alumno:** Ricardo Antonio Benitez Mota
**Variable asignada:** `nivel_bonus_cat`

## Desglose por pregunta

| Pregunta | Pts | Comentario |
|---|---|---|
| P1 | 10/10 | Justificación completa y bien conectada con la magnitud: φ=1.1664>1, Cameron-Trivedi rechaza equidispersión, y explícitamente razona que al ser φ<1.5 "la desviación no es severa" y por eso elige QuasiPoisson. |
| P2 | 7/10 | Identifica correctamente el nivel de mayor riesgo, (10,25] con RF=2.6544 (+165.4%, cálculo correcto), y revisa bien la significancia de todos los niveles. Sin embargo, no identifica explícitamente cuál es el nivel de **menor** riesgo (fuera de la referencia) ni lo traduce a %, que la pregunta pide de forma explícita. |
| P3 | 10/10 | Explicación correcta y completa: ecuaciones de score con offset que igualan siniestros predichos y observados (Σn/Σe), y buen resumen de la ventaja del GLM (multivariable, efecto multiplicativo, incertidumbre estadística). |
| P4 | 10/10 | Explicación técnica correcta y completa: CV constante, corrección de sesgo al modelar log(Y), Lognormal fuera de la familia exponencial natural. |
| P5 | 10/10 | Elección correcta de Binomial Negativa con AIC/BIC bien citados y explicación acertada del pseudo R² bajo, mencionando también la importancia de la capacidad de discriminación. |
| P6 | 9/10 | Buena comparación cuantitativa: RF frecuencia 2.6544 vs RF severidad 1.1708 para (10,25], correctamente interpretado como "misma dirección pero distinta intensidad" — un matiz más preciso que solo decir "misma/distinta dirección", y bien conectado con la justificación de separar Frecuencia×Severidad. |
| P7 | 10/10 | Distingue con precisión calibración (ratio 1.0249) de discriminación (Gini 0.2315), interpretación correcta y completa. |
| P8 | 10/10 | Identificación y cálculos correctos: (10,25] prima más alta ($373.60, factor 2.0489=+104.9%), (-1,0] prima más baja ($118.65, factor 0.6507=−34.9%). |
| P9 | 10/10 | Excelente síntesis: integra RF de frecuencia con su intervalo de confianza (2.5358–2.7785), RF de severidad y prima pura final, con lenguaje técnico defendible ante la CNSF. |

## Redacción: 9/10

## Nota final: 95/100 (calificación: 9.5/10)

## Comentarios generales
Entrega muy sólida: manejas con precisión los conceptos de sobredispersión, comparación de modelos, calibración/discriminación y tarifa, siempre citando tus propios números de `nivel_bonus_cat` sin errores conceptuales. Destaca especialmente P6 y P9 por el nivel de detalle cuantitativo. El único punto a mejorar es P2: te faltó identificar explícitamente el nivel de **menor** riesgo (no solo el de mayor) y traducirlo a porcentaje, tal como pedía la pregunta.
