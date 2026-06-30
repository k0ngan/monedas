# PDDI — Tarea 2: Conteo automático de monedas (yen)

Sistema de conteo automático de monedas **japonesas (yen)** con **técnicas clásicas** de procesamiento
digital de imágenes (Otsu, morfología, watershed, Hough y Fourier). Trabajo individual de la asignatura
**Procesamiento Digital de la Información (INFB6073)** — UTEM.

- **Autor:** Francisco Alejandro Pinto Abraham — RUT 21.571.239-7
- **Universidad:** Universidad Tecnológica Metropolitana (UTEM)

## Contenido

```
images/                                         26 fotografías yen curadas (.jpg)
ground_truth.csv                                conteo real de monedas por imagen
UTEM_2026_1_PDDI_Tarea2_Monedas_Yen.ipynb       notebook ejecutable (Partes I–VII + uso de IA)
```

El notebook aplica además técnicas del material del curso (transformaciones de histograma,
corrección de iluminación por división, Fourier 2D con `scipy.fft`) e incluye una tabla que mapea
cada técnica a su apunte fuente.

## Cómo ejecutar en Google Colab

1. Abre el notebook en Colab.
2. En la primera celda de configuración, ajusta `GITHUB_USER` con tu usuario de GitHub
   (y `REPO` si renombras el repositorio).
3. Ejecuta todo (`Entorno de ejecución → Ejecutar todo`). El notebook clona este repositorio y lee las
   imágenes desde `images/` automáticamente.

## Fuente de los datos

Subconjunto curado de la categoría *yen* de la base de datos pública **Coins Image Dataset**
(imágenes + `coins_count_values.csv` con el conteo real). Las 32 imágenes se eligieron para cubrir
distintos niveles de dificultad: variación de resolución, iluminación, contraste, fondos y solapamiento
entre monedas.
