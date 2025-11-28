
# Reporte de análisis – OCR del periódico *El Martillo* (1916)

## 1. Justificación de la página seleccionada

La página elegida combina varios elementos que resultan útiles para la tarea de OCR:

- Un artículo principal con desarrollo argumentativo (“El periodismo departamental”).
- Fragmentos editoriales vinculados a la identidad y misión del periódico.
- Información de cabecera (título del diario, precio, condiciones de venta).
- Un aviso publicitario de la época (máquinas de coser Singer).

Esta mezcla de texto continuo, bloques cortos y publicidad permite evaluar el comportamiento del modelo en diferentes tipos de contenido dentro de la misma página.

## 2. Desafíos del OCR en esta fuente histórica

Durante el proceso se identificaron varias dificultades propias de un periódico antiguo:

- Tipografía desgastada y tinta irregular, especialmente en las zonas cercanas a los bordes.
- Saltos de línea y guiones por corte de columna que afectan la continuidad de las oraciones.
- Palabras con ortografía antigua o caracteres distorsionados.
- Secciones sin títulos claros, lo que obliga al modelo a inferir si se trata de un artículo, un aviso o simplemente información editorial.

A pesar de ello, el modelo de visión empleado (Gemini) logró recuperar fragmentos coherentes y estructurarlos en un JSON que luego se convirtió en un dataset tabular.

## 3. Resultados obtenidos y distribución del contenido

El OCR permitió identificar al menos cuatro bloques relevantes:

- Un artículo principal con fecha y número de edición.
- Un bloque relacionado con la cabecera del periódico.
- Un texto adicional de carácter más reflexivo o editorial.
- Un anuncio publicitario sobre máquinas de coser.

En el notebook se genera un gráfico de barras que muestra la distribución por tipo de contenido (`article`, `advertisement`, `other`). Aunque la muestra es pequeña, permite visualizar que la página combina contenido informativo y comercial.

## 4. Principales hallazgos

- El periódico articula opinión editorial con avisos comerciales dentro de la misma página, lo que refleja el modelo de financiamiento típico de la prensa de la época.
- El encabezado y la forma de presentar el precio del diario ayudan a reconstruir prácticas de consumo y acceso a la información a inicios del siglo XX.
- El uso de un modelo de IA para OCR facilita convertir estas fuentes históricas en bases de datos reutilizables para futuros análisis cuantitativos y cualitativos.

En conjunto, el ejercicio muestra que es posible pasar de una imagen escaneada a un conjunto de datos estructurado, apto para exploraciones posteriores en historia, prensa y estudios sociales.
