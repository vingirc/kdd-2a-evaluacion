# 2a. Evaluación — Extracción de Conocimiento en Bases de Datos

Alumno: Irving Chaparro Peña
Profesor: Filiberto Ruiz Hernández

## Estructura

- `SA/` — Análisis Supervisado y No Supervisado
  - `01_regresion_beisbol.ipynb` — Regresión (Random Forest Regressor) sobre `beisbol.csv`
  - `02_clasificacion_breast_cancer.ipynb` — Clasificación (Decision Tree) sobre `breast-cancer.csv`
  - `03_agrupacion_samsung.ipynb` — Agrupación (K-Means) sobre `samsung.csv`
  - `04_pca_comprar_alquilar.ipynb` — Reducción de dimensionalidad (PCA) sobre `comprar_alquilar.csv`
- `DE/` — Algoritmos alternos, vistos en clase
  - `01_clasificacion_breast_cancer_alterno.ipynb` — Clasificación (Logistic Regression)
  - `02_regresion_beisbol_alterno.ipynb` — Regresión (Ridge Regression)
- `AU/` — Documento elaborado con herramienta alternativa a Jupyter Notebook (Quarto), rehaciendo los 6 análisis de SA y DE
  - `documento.qmd` / `documento.html`
- `datasets/` — Conjuntos de datos usados
- `models/` — Modelos entrenados (.joblib) y gráficas exportadas (.png)

## Resumen de resultados

| Notebook | Algoritmo | Métrica principal |
|---|---|---|
| SA-1 (regresión, beisbol) | Random Forest Regressor | R² CV = 0.092 |
| SA-2 (clasificación, breast-cancer) | Decision Tree | F1 = 0.895 · ROC-AUC = 0.956 |
| SA-3 (agrupación, samsung) | K-Means (k=2, elegido por silhouette) | Silhouette = 0.431 |
| SA-4 (reducción dim., comprar_alquilar) | PCA | 7/9 componentes para ≥95% var. explicada |
| DE-1 (clasificación alterna, breast-cancer) | Logistic Regression | F1 = 0.964 · ROC-AUC = 0.996 |
| DE-2 (regresión alterna, beisbol) | Ridge Regression | R² CV = 0.209 |
| AU | Los 6 análisis anteriores (SA-1 a SA-4, DE-1, DE-2) rehechos en Quarto | ver `AU/documento.html` |

## Cómo ver el documento AU

`AU/documento.html` es un archivo HTML autocontenido (código, texto y gráficas embebidas) que rehace, con Quarto en vez de Jupyter Notebook, los seis análisis de SA y DE. GitHub no lo renderiza directamente al verlo en el navegador del repositorio — para visualizarlo con estilo, descárgalo y ábrelo localmente, o usa un visor como https://htmlpreview.github.io/ pegando la URL "raw" del archivo.
