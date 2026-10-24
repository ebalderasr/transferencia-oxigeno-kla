---
title: "Anexo para el instructor: determinación de kLa"
autor: "Octavio T. Ramírez · Emiliano Balderas · Instituto de Biotecnología, UNAM"
---

# 1. Preparación del montaje

Preparar el reactor Sartorius de 50 L con 30 L de agua. Verificar el modelo, los límites de agitación y el montaje de impulsor, difusor y sonda. El barrido utiliza 200, 400, 600, 800 y 1000 rpm, con aire a 0.5 vvm, equivalente a 15 L/min. Mantener constantes temperatura, presión y composición del líquido. Registrar sus valores sin asignar una temperatura que no se haya confirmado.

La versión original de estas notas utiliza N₂ para preparar cada reoxigenación. Confirmar antes del taller que el suministro y la conmutación permiten repetir la maniobra en todas las velocidades. Verificar el flujo de N₂ adecuado al montaje y registrarlo; no confundirlo con la especificación de aire a 15 L/min. No añadir un reactivo consumidor de oxígeno para acelerar la preparación, pues cambiaría el balance utilizado.

Comprobar calibración y acondicionamiento de la sonda según su modelo. Registrar filtrado y frecuencia de adquisición. Mantener inactivo el control de oxígeno y cualquier cascada que cambie rpm o gases. El control de temperatura puede mantenerse activo. Confirmar que el venteo esté libre y que las líneas no presuricen el recipiente.

El instructor opera cilindros, reguladores y conmutación de gases. Utilizar N₂ con ventilación adecuada y conforme al procedimiento del laboratorio; puede desplazar el oxígeno ambiental. Mantener accesibles los elementos de operación y evitar maniobras de los participantes sobre líneas o conexiones no destinadas a ello.

# 2. Organización de los equipos

Reservar 30–45 minutos por equipo. El barrido se completó en aproximadamente 30 minutos en la prueba de laboratorio, según el relato de preparación; prever tiempo adicional para cálculos y discusión. Asignar tareas de operación, tiempo, adquisición, condiciones, cálculo y verificación. Iniciar el análisis mientras se adquieren las siguientes curvas.

Preparar una copia de la guía por equipo o participante y una sola copia de este anexo. La hoja de cálculo contiene cinco velocidades; disponer de una copia del archivo por equipo para conservar sus resultados.

No exigir una duración fija por curva. Si una reoxigenación no alcanza una meseta, registrar la duración y tratarla como incompleta. No introducir un valor final supuesto para obtener un resultado. Una condición repetida es útil si el tiempo lo permite, pero el barrido básico no incluye réplicas obligatorias.

# 3. Criterios de análisis

La regresión utiliza $Y=\ln[(y_\infty-y_0)/(y_\infty-y)]$ y tiempo en segundos. La pendiente tiene unidades s⁻¹ y se multiplica por 3600 para reportar h⁻¹. La ordenada al origen queda libre. El intervalo inicial de análisis es 20–80 % del recorrido entre las mesetas; revisar las curvas antes de aceptar la selección automática.

El cambio N₂ → aire puede introducir un retraso por las líneas y la sustitución del gas. Marcar la maniobra y revisar el comienzo efectivo de la reoxigenación. Excluir del ajuste el tramo de conmutación si no cumple la composición gaseosa constante. Una ordenada libre permite un desplazamiento temporal, pero no corrige cambios de composición dentro del tramo ajustado ni una sonda lenta.

La plantilla exige al menos tres puntos para mostrar el ajuste, como mínimo de cálculo. Tres puntos no bastan para asegurar una estimación confiable: solicitar más muestras y revisar que el tramo cubra una parte apreciable de la transición. No aumentar la confianza solo por obtener un R² alto.

| Observación | Revisión |
|---|---|
| Agua ya saturada antes del registro | Desoxigenar y obtener una nueva reoxigenación a rpm constantes. |
| No hay meseta final | Prolongar el registro; si no se logra, conservar el ensayo como incompleto. |
| Y tiene curvatura | Revisar equilibrio elegido, conmutación de gas, sonda y condiciones de operación. |
| Logaritmo indefinido | Comprobar y∞, unidades y lecturas iguales o superiores a la meseta. |
| Pocos puntos a rpm altas | Usar el menor intervalo digital disponible; revisar la respuesta de la sonda. |
| kLa no crece con rpm | Revisar caudal, temperatura, dispersión, registros y ajuste antes de atribuir una causa física. |
| Diferencias entre equipos | Comparar condiciones y criterios de selección; no atribuirlas solo a la operación. |

# 4. Respuesta de la sonda y alcance del resultado

El balance supone que la medición sigue la concentración del líquido con rapidez suficiente. La escala de tiempo de transferencia es $1/k_La$. Si la sonda y el filtrado responden en tiempos comparables, el resultado incluye su dinámica. Esta limitación puede ser más visible en las velocidades altas. La práctica de respuesta de sensores permite discutir esta diferencia, pero no debe usarse una constante de otra sonda como corrección de este reactor.

Los valores obtenidos describen agua, volumen, geometría y condiciones del ensayo. No son especificaciones universales del reactor ni parámetros directamente transferibles a un cultivo celular. En presencia de células, el balance incluye OUR y el procedimiento de análisis debe adaptarse.

# 5. Datos experimentales pendientes

Los registros ya fueron capturados en el laboratorio, pero no están disponibles en este proyecto al preparar la guía. No se incluyen valores de kLa, curvas históricas ni resultados simulados como sustituto. Al recibir los datos, conservar los archivos originales, identificar cada velocidad y revisar tiempo, oxígeno, mesetas, caudal y temperatura antes de calcular.

La tabla ilustrativa del documento de origen no se trasladó: sus valores transformados no coinciden con todas las lecturas de oxígeno indicadas. La guía utiliza las ecuaciones y hojas vacías para trabajar con las mediciones del taller.

# 6. Fuentes del material

El fundamento se adaptó de las notas técnicas de determinación de kLa incluidas en este proyecto. El formato corresponde a las prácticas de respuesta de sensores y control de oxígeno. La bibliografía del documento de origen se conserva allí para consulta; los resultados del taller se documentarán con sus propios registros.
