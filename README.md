# PDDI — Tarea 2: Conteo automático de monedas (yen)

Sistema de conteo automático de monedas **japonesas (yen)** con **técnicas clásicas**, usando
**exclusivamente los métodos vistos en clase** (Colabs del curso): `rgb2gray` + realce gamma → umbral de
Otsu → morfología de `skimage` (disco) → `measure.label` + `regionprops` (área + excentricidad) →
bounding boxes; k-means de color como segunda segmentación; y Fourier 2D con `scipy.fft`. Trabajo
individual de la asignatura **Procesamiento Digital de la Información (INFB6073)** — UTEM.

- **Autor:** Francisco Alejandro Pinto Abraham — RUT 21.571.239-7
- **Universidad:** Universidad Tecnológica Metropolitana (UTEM)

## Contenido

```
images/                                         26 fotografías yen curadas (.jpg)
ground_truth.csv                                conteo real de monedas por imagen
UTEM_2026_1_PDDI_Tarea2_Monedas_Yen.ipynb       notebook ejecutable (Partes I–VII + uso de IA)
```

El notebook incluye una tabla que mapea cada técnica al Colab del curso que la introduce (Clase 16:
conteo de monedas, morfología, `regionprops`; Clase 15: k-means; Clases 05–10: Fourier). No se usan
watershed, Hough ni CLAHE por no haberse revisado en clase.

## Cómo ejecutar en Google Colab

1. Abre el notebook en Colab.
2. En la primera celda de configuración, ajusta `GITHUB_USER` con tu usuario de GitHub
   (y `REPO` si renombras el repositorio).
3. Ejecuta todo (`Entorno de ejecución → Ejecutar todo`). El notebook clona este repositorio y lee las
   imágenes desde `images/` automáticamente.

## Fuente de los datos

Subconjunto curado de la categoría *yen* de la base de datos pública **Coins Image Dataset**
(imágenes + `coins_count_values.csv` con el conteo real). Las 26 imágenes se eligieron para cubrir
distintos niveles de dificultad: variación de resolución, iluminación, contraste, fondos y solapamiento
entre monedas.
