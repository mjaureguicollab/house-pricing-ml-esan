# house-pricing-ml-esan
Proyecto final de Machine Learning para predicción pre-venta de precios de viviendas.
# House Pricing - Predicción pre-venta de precios de viviendas

## Machine Learning & Deep Learning - ESAN

Proyecto final desarrollado en  Google Colab para estimar
el precio de venta de viviendas utilizando Machine Learning.

## Objetivo

Construir un modelo capaz de estimar el precio de una vivienda
utilizando exclusivamente información disponible antes de la venta.

El modelo se plantea como un sistema de apoyo a la tasación inicial,
no como sustituto de una tasación profesional.

## Dataset

El proyecto utiliza el dataset House Prices, compuesto por:

- 1,460 viviendas
- 81 variables originales
- 75 predictores utilizados en el modelo
- Variable objetivo: SalePrice

## Metodología

El proyecto contempla:

1. Análisis exploratorio de datos
2. Tratamiento de valores faltantes
3. Feature Engineering
4. Prevención de data leakage
5. Codificación de variables categóricas
6. Escalamiento de variables numéricas
7. Comparación de modelos
8. Optimización de XGBoost
9. Evaluación en validación
10. Evaluación final en test
11. Análisis de errores e interpretación

## Modelos evaluados

- Ridge
- Extra Trees
- XGBoost
- Ensemble ponderado

## Modelo seleccionado

XGBoost ajustado mediante búsqueda de hiperparámetros.

### Mejor configuración

- learning_rate = 0.05
- max_depth = 3
- min_child_weight = 3
- subsample = 0.75
- colsample_bytree = 0.70
- reg_lambda = 1.0
- reg_alpha = 0.05

## Resultados

### Validación

| Modelo | MAE | RMSE | RMSLE |
|---|---:|---:|---:|
| XGBoost | $13,397.73 | $19,731.16 | 0.1189 |
| Ensemble | $13,397.73 | $19,731.16 | 0.1189 |
| Ridge | $17,031.37 | $24,542.08 | 0.1420 |
| Extra Trees | $17,115.15 | $25,140.86 | 0.1508 |

### Test

- MAE: $16,205.48
- RMSE: $28,249.16
- RMSLE: 0.1437
- Sesgo: -$869.15

## Principales variables

Las variables con mayor importancia predictiva fueron:

1. OverallQual
2. TotalSF
3. HasFireplace
4. ExterQual
5. KitchenQual

## Principales conclusiones

XGBoost presentó el mejor desempeño dentro de las alternativas
evaluadas y fue seleccionado por su combinación de desempeño,
capacidad para capturar relaciones no lineales y simplicidad
operativa frente al ensemble.

El modelo debe utilizarse como herramienta de apoyo a la decisión
y no como sustituto de una tasación profesional.

## Tecnologías

- Python
- Google Colab
- pandas
- NumPy
- scikit-learn
- XGBoost
- Matplotlib
- Seaborn

## Autores

Proyecto desarrollado por un equipo de 4 integrantes.
Manuel Jauregui
Gonzalo Majluf
Jordi Moreno
Maritza Aredo

## Presentación

La presentación final se encuentra en:

`presentation/House_Pricing_Presentacion.pptx`
