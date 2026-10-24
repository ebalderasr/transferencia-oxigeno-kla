# Preparación y mantenimiento

## Fuentes

`practica/Practica_kLa.md` contiene la guía y `practica/Anexo_instructor.md`, las notas para el instructor. `practica/generar_word.py` convierte ambas fuentes con Pandoc y aplica el formato común de la serie. La opción `--pdf` exporta ambos documentos con LibreOffice. La plantilla de estilo se conserva en la raíz.

El esquema `figuras/01_barrido_kLa.png` describe el procedimiento y no representa una curva experimental. No hay datos originales de laboratorio disponibles en esta entrega.

## Plantilla de cálculo

`practica/generar_calculo.py` genera `practica/Calculo_kLa.xlsx` mediante openpyxl. Las entradas son tiempo en segundos, lectura de oxígeno, mesetas inicial y final y datos del montaje. Hay 300 filas disponibles por condición. Para registros más largos, ampliar fórmulas, rangos de regresión y referencias de gráficas; no descartar ni espaciar muestras sin revisar la resolución necesaria.

Se calcula el recorrido normalizado, la transformación logarítmica y el ajuste lineal con ordenada libre. Se seleccionan inicialmente puntos del 20–80 % del recorrido. Se requieren tres puntos como mínimo de cálculo; la suficiencia experimental se revisa en la curva y los residuos. kLa [h⁻¹] = 3600 × pendiente [s⁻¹]. La hoja no corrige automáticamente la dinámica de la sonda ni el retraso de la línea de gas.

Las fórmulas se evalúan al abrir el archivo en una aplicación de hoja de cálculo. No se introducen resultados precalculados. Conservar el archivo original de adquisición y trabajar en una copia de la plantilla. No ejecutar el generador sobre una plantilla ya rellenada sin respaldarla.

## Incorporación de datos

Al disponer de los registros, conservarlos sin modificar. Documentar unidades de tiempo y oxígeno, rpm efectivas, caudal, temperatura, cambios de gas y procedencia del archivo. Identificar cada reoxigenación y comprobar mesetas antes de llenar la plantilla. No atribuir al registro condiciones no documentadas ni asumir que 100 % coincide con el equilibrio.

La duración prevista es 30–45 minutos por equipo. El cronograma se apoya en la prueba de barrido de unos 30 minutos comunicada por Emiliano; no permite reconstruir datos ni tiempos individuales de las curvas ausentes.

## Verificación de esta entrega

Se comprobaron la ausencia de datos precargados, las referencias de las fórmulas, las cinco velocidades y las conversiones de unidades. El procedimiento matemático recuperó 72 h⁻¹ para una señal exponencial de comprobación generada fuera de los entregables. Se revisó visualmente la exportación de las ecuaciones a PDF. Este entorno dispone de LibreOffice Writer, pero no puede abrir la plantilla con Calc; queda pendiente verificar el recálculo y la representación de las gráficas en Excel o LibreOffice Calc. La comprobación matemática no sustituye esa prueba de la aplicación.
