# Determinación de kLa en un biorreactor agitado

Material del taller de transferencia de oxígeno. Cada equipo obtiene curvas de reoxigenación a 200, 400, 600, 800 y 1000 rpm, calcula un kLa por condición y construye un barrido de kLa frente a rpm.

| Condición | Valor |
|---|---|
| Reactor | Sartorius, capacidad nominal de 50 L; modelo por registrar |
| Volumen | 30 L de agua |
| Aire durante la reoxigenación | 0.5 vvm = 15 L/min, constante |
| Preparación de cada curva | Desoxigenación con N₂ y sustitución por aire |
| Duración | 30–45 min por equipo |

| Simposio | Curso avanzado |
|:---:|:---:|
| [![XI Simposio Latinoamericano de Tecnología de Cultivos Celulares](docs/imagenes/Simposio_portada.png)](https://www.slatcc.com/) | [![Curso Avanzado de Tecnologías de Cultivo Celular 2026](docs/imagenes/Curso_portada.png)](https://www.slatcc.com/) |

## Material para imprimir y calcular

- [Guía para participantes, PDF](practica/Practica_kLa.pdf) y [Word](practica/Practica_kLa.docx): fundamentos, procedimiento, hojas de datos y barrido.
- [Anexo para el instructor, PDF](practica/Anexo_instructor.pdf) y [Word](practica/Anexo_instructor.docx): preparación, revisión de ajustes y limitaciones. Imprimir una copia.
- [Plantilla de cálculo](practica/Calculo_kLa.xlsx): cinco hojas de adquisición y cálculo, curvas, ajustes, residuos y resumen gráfico.

Los registros capturados en el laboratorio aún no se incorporan. Los documentos y la plantilla no contienen resultados experimentales supuestos.

## Generación de documentos

Instalar Python 3 y las dependencias de `requirements.txt`, además de Pandoc y LibreOffice:

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python practica/generar_word.py --pdf
python practica/generar_calculo.py
```

El generador de documentos usa los Markdown de `practica/` y `plantilla_documento.docx`. Conserva el formato de las prácticas de respuesta de sensores y control de oxígeno. Regenerar sobrescribe los archivos de salida; incorporar primero las ediciones manuales de Word a sus fuentes. El generador de cálculo crea una plantilla vacía y sobrescribe el Excel; guardar los registros de cada equipo en copias independientes.

Los autores aparecen como Octavio T. Ramírez y Emiliano Balderas, Instituto de Biotecnología, UNAM. El documento original de notas técnicas se conserva en la raíz.

## Prácticas relacionadas

- [Respuesta de sensores en bioprocesos](https://github.com/ebalderasr/respuesta-sensores-bioprocesos).
- [Control de oxígeno en biorreactores](https://github.com/ebalderasr/control-oxigeno-biorreactores).
