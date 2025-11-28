# OCR del periódico *El Martillo* (1903–1919)  
Digitalización y análisis con Google Gemini

Este repositorio contiene el proceso de digitalización, extracción de texto y análisis estructurado de una página del periódico histórico peruano *El Martillo*, publicado en Chiclayo entre 1903 y 1919. El propósito es transformar una imagen escaneada antigua en datos estructurados (CSV) mediante técnicas modernas de reconocimiento óptico de caracteres (OCR) basadas en modelos de inteligencia artificial.

## Metodología general

1. **Carga de la imagen:**  
   La imagen seleccionada se descarga directamente desde GitHub mediante su enlace RAW para asegurar reproducibilidad. No se depende de cargas manuales en Colab.

2. **Ejecución del OCR:**  
   Se utiliza el modelo `gemini-2.0-flash` del servicio Google AI Studio.  
   Este modelo permitió extraer titulares, fragmentos de artículos, anuncios y textos editoriales presentes en la página.

3. **Conversión del resultado:**  
   El modelo devuelve un JSON estructurado, el cual se transforma en un DataFrame y posteriormente en un archivo CSV.  
   Las columnas generadas son:  
   - `date`  
   - `issue_number`  
   - `headline`  
   - `section`  
   - `type`  
   - `text_excerpt`

4. **Análisis exploratorio básico:**  
   Se incluye un gráfico sencillo que resume los tipos de contenido identificados en la página (artículos, avisos, otros).

## Notas metodológicas
No se utilizó el modelo Claude (Anthropic) debido a que su API requiere créditos de pago o aprobación previa.  
En este trabajo se optó por Google Gemini porque permite trabajar con imágenes y generar OCR de manera más accesible y sin fricciones para efectos prácticos de la tarea.

## Requerimientos
Las bibliotecas necesarias para ejecutar el notebook son:
google-genai
pandas
matplotlib
pillow
requests

## Entregables
- Notebook con todo el proceso de OCR y análisis.
- Dataset estructurado en formato CSV.
- Imagen original utilizada.
- Reporte resumen del proyecto ubicado en outputs/report.md.
