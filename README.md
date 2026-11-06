# 🔬 Práctica Didáctica: Visión Artificial Aplicada al Control de Levitador magnético (STEM - Bachillerato)

**Autor:** Prof. Camilo Flores Rodríguez  
**Áreas:** Visión por Computadora, Electrónica, Mecatrónica, Pensamiento Matemático.  
**Nivel Educativo:** Bachillerato (Taller de Ciencias II y Electrónica / Proyectos STEM Integrados).

**Proyecto:** Levitador acústico.  
**Entorno de Ejecución:** Python 3 | OpenCV | NumPy | Matplotlib | Google Colab.

---

## 📌 Presentación del Recurso Pedagógico

Este repositorio contiene una unidad didáctica práctica diseñada para estudiantes de bachillerato en el marco de la enseñanza de la **Visión Artificial y el Procesamiento Digital de Imágenes**, aplicada directamente al monitoreo y control óptico en tiempo real de **prototipos mecatrónicos (Levitadores Acústicos y Magnéticos, Drones y Grúas)**.

El cuaderno de trabajo implementado en **Google Colab** permite a los estudiantes experimentar desde cero con imágenes reales, guiándolos a través de los conceptos fundamentales de visión por computadora sin requerir conocimientos previos avanzados de programación.

---

## 🎯 Objetivos de Aprendizaje Integrados (STEM)

1. **Ingeniería y Robótica:** Comprender cómo una cámara actúa como un sensor telemétrico de posición para realimentar bucles de control en sistemas en suspensión.
2. **Ciencias / Física:** Relacionar variables de espacio, aceleración, gravedad y calibración física ($px \rightarrow mm$).
3. **Pensamiento Matemático:** Estudiar representaciones matriciales de imágenes, transformaciones geométricas, cálculo de momento de masas ($M_{00}, M_{10}, M_{01}$) y estadística aplicada ($CV$).
4. **Tecnología / Programación:** Manipular librerías estándar en la industria (`OpenCV`, `NumPy`) para segmentación, filtrado y extracción de contornos.

---

## 📂 Contenido de la Clase / Secuencia Didáctica

La práctica se divide en **8 fases secuenciales y auto-explicativas**:

1. **Paso 1: Adquisición de Datos y Representación Digital:** Carga automática de imágenes reales descargadas directamente a través de URL y análisis de arreglos multidimensionales (matrices).
2. **Paso 2: Modelos de Color (BGR vs. HSV):** Experimentación práctica para desacoplar el tono ($H$) de las variaciones de intensidad lumínica ($V$) y sombras del laboratorio.
3. **Paso 3: Segmentación por Umbralización (*Thresholding*):** Creación de máscaras binarias ($0$ y $255$) para aislar la silueta del objeto suspendido.
4. **Paso 4: Filtrado y Suavizado Gaussiano (*Gaussian Blur*):** Aplicación de matrices de convolución con distribución gaussiana ($5 \times 5$) para atenuar ruido digital previo a la extracción de bordes.
5. **Paso 5: Detección de Bordes (Sobel vs. Canny):** Comparación cualitativa y matemática entre derivadas discretas (Sobel) y el pipeline del algoritmo Canny ($1\text{ px}$ de grosor).
6. **Paso 6: Sustracción de Fondo (*Background Subtraction*):** Operación de resta matricial de imágenes (`cv2.absdiff`) para detectar desplazamientos dinámicos respecto a una imagen patrón.
7. **Paso 7: Momentos de Imagen y Centro de Masa:** Determinación de las coordenadas $(C_x, C_y)$ del centro de masa de la partícula mediante `cv2.moments()` y cálculo del área envolvente con `cv2.contourArea()`.
8. **Paso 8: Calibración Telemétrica ($px/mm$):** Estimación de la constante de conversión espacial y cálculo de la altura física de levitación en milímetros reales.

---

## 🛠️ Tecnologías y Herramientas Utilizadas

- **Python 3.x**
- **OpenCV (`cv2`):** Procesamiento de imágenes, espacio HSV, contornos y transformaciones.
- **NumPy:** Manipulación matricial y operaciones algebraicas de baja latencia.
- **Matplotlib:** Visualización de canales, histogramas y comparativas gráficas.
- **Google Colab / Jupyter Notebooks:** Entorno interactivo y accesible sin instalación previa local.

---

## 🚀 Cómo Ejecutar esta Práctica

1. Da clic en el siguiente enlace: https://colab.research.google.com/drive/1b4JXlzs2Aaj2fwkGYBvwsxTHKaHdrMAb?usp=sharing
2. Ejecuta las celdas en orden. El cuaderno descargará automáticamente las imágenes de muestra desde Internet y procesará todas las fases sin necesidad de configuraciones adicionales.

---

## 💡 Metodología de Integración en el Aula

Esta clase forma parte del **Marco de Evaluación Transversal 80/20**, donde los alumnos combinan un 80% de desarrollo técnico-práctico en electrónica/matemáticas con un 20% de habilidades de pensamiento creativo e innovación (metodologías CPS y reencuadre de problemas). Los resultados de este cuaderno sirven como la memoria de cálculo del módulo de percepción en el proyecto integrador final del semestre Levitador Magnético.
