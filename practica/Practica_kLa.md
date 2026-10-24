---
title: "Determinación de kLa en un biorreactor agitado"
autor: "Octavio T. Ramírez · Emiliano Balderas · Instituto de Biotecnología, UNAM"
---

**Taller:** Transferencia de oxígeno en biorreactores

**Duración:** 30–45 min por equipo, incluidos registro y cálculos.

**Equipo:** reactor Sartorius de 50 L con 30 L de agua. Registrar modelo e identificación disponibles.

# 1. Objetivo

Determinar el coeficiente volumétrico de transferencia de oxígeno, kLa, mediante reoxigenación de agua a distintas velocidades de agitación. Cada equipo obtendrá una curva por velocidad, calculará el kLa correspondiente y construirá un barrido de kLa frente a rpm, con el volumen y la aireación constantes.

# 2. Transferencia de oxígeno

El oxígeno pasa de las burbujas al líquido cuando su concentración en el agua es menor que la concentración de equilibrio con el gas. La velocidad volumétrica de transferencia se expresa como:

$$\mathrm{OTR}=k_La\,(C^*-C_L)$$

$C^*$ es la concentración en equilibrio con el aire y $C_L$ la concentración en el líquido. El término $C^*-C_L$ es la fuerza impulsora. Si las concentraciones se expresan en mg/L y kLa en h⁻¹, OTR tiene unidades de mg de O₂ por litro y hora.

El coeficiente $k_La=k_L\,a$ combina el transporte a través de la película líquida y el área de contacto gas–líquido por unidad de volumen. Depende de agitación, caudal, geometría y propiedades del líquido. En esta práctica se estudia el efecto de la agitación; el volumen y el caudal de aire se mantienen fijos.

Un kLa mayor permite una transferencia mayor para la misma fuerza impulsora. En un cultivo, además hay consumo celular, OUR. La concentración permanece constante cuando OTR y OUR se igualan. Aquí se utiliza agua sin células y se supone despreciable el consumo de oxígeno.

# 3. Condiciones de operación

| Parámetro | Condición |
|---|---|
| Reactor | Sartorius, capacidad nominal de 50 L |
| Volumen de trabajo | 30 L de agua |
| Aireación durante la reoxigenación | 0.5 vvm constantes = **15 L/min** |
| Agitación del barrido | 200, 400, 600, 800 y 1000 rpm |
| Temperatura | Registrar y mantener constante durante el barrido |
| Presión | Registrar la disponible y mantener las mismas condiciones de venteo |
| Consumo biológico | Sin células |
| Control de oxígeno | Desactivado; ninguna cascada debe cambiar rpm o gases |
| Registro | Oxígeno, tiempo, rpm, caudal y temperatura; adquisición digital preferentemente cada 1 s |

vvm expresa litros de gas por litro de líquido y minuto. El caudal se calcula con los **30 L de trabajo**, no con la capacidad nominal: $0.5\times30=15$ L/min. Registrar la referencia del caudalímetro o controlador de flujo disponible.

La secuencia propuesta es ascendente, con una curva independiente en cada nivel. Durante cada reoxigenación las rpm permanecen constantes. No se obtiene un kLa por nivel cambiando las rpm sobre una única curva ni aumentando la agitación cuando el agua ya está saturada.

![Secuencia del barrido a volumen y aireación constantes](../figuras/01_barrido_kLa.png)

# 4. Método dinámico de reoxigenación

El método consiste en reducir el oxígeno disuelto con N₂ y después sustituirlo por aire. Se registra el aumento de oxígeno hasta alcanzar una meseta. La aireación de 0.5 vvm corresponde a la etapa con aire; el nitrógeno se utiliza para preparar cada ensayo y no se mantiene durante la reoxigenación.

Para agua sin consumo apreciable y con condiciones constantes:

$$\frac{dC_L}{dt}=k_La\,(C^*-C_L)$$

Esta es una ecuación diferencial de primer orden. Si la concentración inicial es $C_0$, su solución es:

$$C_L(t)=C^*-(C^*-C_0)e^{-k_La(t-t_0)}$$

La constante de tiempo del modelo es $\tau=1/k_La$, usando unidades de tiempo compatibles. En una τ se recorre el $1-e^{-1}\approx63.2\,\%$ del cambio. Aquí τ describe la transferencia observada en el reactor; no es la constante de tiempo de la sonda aislada.

## Transformación para el ajuste lineal

Al reorganizar la solución:

$$Y(t)=\ln\left(\frac{C^*-C_0}{C^*-C_L(t)}\right)=k_La\,(t-t_0)$$

Si la lectura de oxígeno es proporcional a la concentración, podemos utilizar las lecturas de la pantalla en una misma escala:

$$Y(t)=\ln\left(\frac{y_\infty-y_0}{y_\infty-y(t)}\right)$$

$y_0$ es la lectura inicial, $y_\infty$ la meseta final con aire y $y(t)$ la lectura durante el ascenso. Usar la meseta observada en las condiciones del ensayo; no sustituirla automáticamente por 100 %. La escala y las condiciones deben permanecer constantes.

Se ajusta una recta $Y=a+b\,(t-t_0)$; su pendiente $b$ estima kLa. Se permite una ordenada al origen para revisar posibles desplazamientos temporales y desviaciones del modelo, sin forzar la recta a pasar por cero.

| Unidad del tiempo en la regresión | Unidad de la pendiente | Conversión a h⁻¹ |
|---|---|---|
| Segundos | s⁻¹ | kLa [h⁻¹] = 3600 × pendiente |
| Minutos | min⁻¹ | kLa [h⁻¹] = 60 × pendiente |

La transformación requiere $y_\infty>y_0$ y $y(t)<y_\infty$. Cerca de la meseta, una diferencia pequeña entre lectura y equilibrio amplifica el ruido del logaritmo. No calcular el logaritmo de cero ni de valores negativos.

## Selección del tramo

Como criterio inicial del taller, ajustar la parte comprendida entre el 20 y el 80 % del recorrido observado:

$$r(t)=\frac{y(t)-y_0}{y_\infty-y_0},\qquad 0.20\leq r(t)\leq0.80$$

Estos porcentajes corresponden al cambio entre las mesetas, no necesariamente a 20 y 80 % de saturación. Revisar que el tramo sea aproximadamente lineal, que las rpm y el aire sean constantes y que haya suficientes muestras. El intervalo es un criterio de análisis; puede requerir revisión con el instructor si el inicio tiene un retraso evidente o el ajuste muestra curvatura.

# 5. Organización y procedimiento

Distribuir las tareas de operación, tiempo, adquisición, revisión de condiciones, cálculo y verificación. La maniobra de gases se realiza con el instructor.

| Tiempo orientativo | Actividad |
|---|---|
| 0–5 min | Identificar equipo y sonda; verificar volumen, aire, temperatura, adquisición y salidas en manual. |
| 5–30 min | Registrar las cinco curvas, con desoxigenación y reoxigenación en cada velocidad. Calcular conforme se obtienen los registros. |
| 30–40 min | Revisar mesetas y ajustes, completar la tabla y construir el barrido. |
| 40–45 min | Comparar resultados y documentar curvas incompletas o incidentes. |

La adquisición del barrido se probó en el laboratorio en aproximadamente 30 minutos, según las notas de preparación del taller. Reservar hasta 45 minutos para que cada equipo complete el análisis. Los tiempos por curva dependen de la respuesta observada; no sustituir una meseta ausente por el último dato para cumplir el cronograma.

## Secuencia por velocidad

1. Seleccionar las rpm del ensayo y mantenerlas constantes durante la preparación y la reoxigenación. Confirmar que el control de oxígeno no actúe sobre agitación ni gases.
2. Desoxigenar con N₂ hasta una lectura baja y aproximadamente estable. Una lectura inferior al 10 % de saturación es una referencia operativa; no se requiere forzar el cero. Registrar el nivel alcanzado.
3. Mantener activo el registro y sustituir N₂ por aire a **15 L/min**. Marcar la hora de la maniobra, conservar las rpm y comprobar el caudal real. No mezclar deliberadamente ambos gases durante la reoxigenación.
4. Registrar el ascenso y continuar hasta una meseta final aproximadamente estable. Conservar el registro completo, incluyendo el cambio de gas. Anotar retrasos de líneas, cambios de presión, burbujas en la sonda o cualquier maniobra adicional.
5. Estimar $y_0$ a partir del tramo bajo previo al cambio y $y_\infty$ a partir de la meseta final. Anotar los intervalos usados. Trabajar con promedios de varias lecturas, no con un punto aislado.
6. Calcular el recorrido normalizado y la transformación Y. Seleccionar el tramo de ajuste, obtener pendiente, ordenada al origen y R², y convertir kLa a h⁻¹. Revisar la curva original y los residuos del ajuste.
7. Cambiar a las siguientes rpm y repetir la secuencia completa. Si una curva no permite estimar el equilibrio o presenta cambios de condiciones, conservarla y anotar el motivo por el que no se calcula kLa.

Se realizará una curva por nivel como barrido de taller. Si queda tiempo, repetir una condición para examinar reproducibilidad. Una sola curva por nivel no permite estimar la variabilidad entre repeticiones.

# 6. Hoja de datos

**Equipo:** ______ **Fecha/hora:** ______ **Responsable:** ______

| Información | Registro |
|---|---|
| Reactor: modelo e ID | |
| Sonda de oxígeno: fabricante, modelo e ID | |
| Calibración, referencia de saturación y filtrado disponibles | |
| Volumen real [L] | |
| Agua: procedencia y adiciones | |
| Temperatura [°C] y presión disponible | |
| Caudal de aire y referencia del instrumento | |
| Impulsor, difusor y posición de sonda disponibles | |
| Archivo y frecuencia real de adquisición | |

## Registro individual de curva

Completar este bloque para cada velocidad y conservar el archivo digital completo.

**RPM:** ______ **Hora del cambio N₂ → aire:** ______ **Aire [L/min]:** ______

**Intervalo inicial:** ______ **y₀:** ______ **Intervalo final:** ______ **y∞:** ______

| Tiempo desde el cambio [s] | Oxígeno [% de saturación] | Recorrido r | Y = ln[(y∞ − y₀)/(y∞ − y)] | Usado en el ajuste |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |

**Tramo ajustado [s]:** ______ **Número de puntos:** ______ **Pendiente [s⁻¹]:** ______

**kLa [h⁻¹]:** ______ **Ordenada al origen:** ______ **R²:** ______

**Incidentes y revisión del ajuste:** ________________________________________

## Resultados del barrido

| RPM | Aire [L/min] | Temperatura [°C] | y₀ / y∞ [%] | Tramo [s] | kLa [h⁻¹] | R² / observaciones |
|---|---|---|---|---|---|---|
| 200 | 15 | | | | | |
| 400 | 15 | | | | | |
| 600 | 15 | | | | | |
| 800 | 15 | | | | | |
| 1000 | 15 | | | | | |

# 7. Análisis y entrega

Para cada velocidad, presentar la curva de oxígeno frente al tiempo y la gráfica de Y con su recta ajustada. Construir después una gráfica de dispersión con **rpm en el eje horizontal y kLa [h⁻¹] en el vertical**. Identificar equipo, volumen, caudal y temperatura. Los puntos pueden unirse para facilitar la lectura; esa línea no constituye por sí sola un modelo de predicción.

La plantilla `Calculo_kLa.xlsx` contiene una hoja por velocidad y un resumen del barrido. Los campos de tiempo y oxígeno se llenan con el registro real; las mesetas inicial y final se introducen después de revisar cada curva. La plantilla utiliza segundos y el intervalo de 20–80 % del recorrido como selección inicial. No contiene datos experimentales ni resultados de referencia.

Un R² elevado no demuestra por sí solo que la medición sea válida. Revisar también curvatura, residuos, resolución temporal, estabilidad del aire y la temperatura, y respuesta de la sonda. Si la transferencia es tan rápida que la dinámica de la sonda resulta comparable, reportar el resultado como una estimación aparente y discutir la limitación.

# 8. Discusión

1. ¿Cómo cambió kLa con las rpm a caudal y volumen constantes? ¿Qué condiciones podrían explicar una tendencia irregular?
2. ¿Por qué disminuye la velocidad de aumento del oxígeno al acercarse a la saturación?
3. ¿Qué efecto tendría usar 100 % como equilibrio si la meseta observada fuera diferente?
4. ¿Qué limita el cálculo cuando una curva tiene pocos puntos o no llega a una meseta?
5. ¿Por qué no basta comparar las rpm de reactores con distinta geometría o volumen?
6. ¿Cómo cambiaría la interpretación en un medio con proteínas, antiespumante o células que consumen oxígeno?
7. ¿Por qué un kLa alto en agua no demuestra por sí solo que un cultivo CHO tendrá oxígeno suficiente?
