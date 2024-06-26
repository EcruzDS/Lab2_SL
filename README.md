# Proyecto de Curso Statistical Learning
## Ejecución proyecto de curso de Statistical Learning
### Para el proyecto final del curso se ha elegido un dataset de una cartera crediticia de una entidad financiera con el fin de analizar sus variables relacionadas con la rentabilidad de cada segmento comercial existente el cual se espera sea la variable Target para posterior crear un modelo relacionado con la rentabilidad por cliente, segmento o producto.

El dataset cuenta con 66 campos y 2819 filas, se adjunta descripción de cada uno de los campos del dataset, que cuenta con variables que describen el Id del crédito, nombre de cliente, fecha de inicio de operación, fecha de vencimiento, saldo del crédito a la fecha de reporte, tasa del crédito, segmentos, análisis de rentabilidad tales como TIR, FTP, incremento de tasa, plazos, pérdida crediticia esperada, entre otros.

### Resultados
Se desarrollo el modelo de clasificación mediante la construcción de algoritmos evaluando distintos hiper-parámetros, con el fin de buscar el modelo óptimo para el caso de la cartera crediticia identificada. A continuación, se comparte información de algunos de los mejores modelos de algoritmos de clasificación:

#### 1. AdaBoost (Adaptive Boosting) resultó favorable en cada una de sus iteraciones comparado con el resto de modelos, con un Roc Auc Score de 96.91% y accuracy del 96.69%, con la optimización de hiperparámetros, se alcanzó: Mejores hiperparámetros: {'base_estimator__max_depth': 1, 'learning_rate': 1, 'n_estimators': 50} ada_hyp_opt.best_score_ = 99.94%
#### 2. LGBM (Light Gradient Boosting Maching) resultó ser otro modelo que mejoró el accuracy, así como su eficiencia al ejecutar.  Roc_Auc Score: 98.72%, Accuracy: 098.35%. Con la optimización de hiperparámetros se alcanzó: Mejores hiperparámetros: {'lgbm__colsample_bytree': 0.9760935678030516, 'lgbm__learning_rate': 0.13487080962675865, 'lgbm__max_depth': 4, 'lgbm__min_child_samples': 25, 'lgbm__n_estimators': 77, 'lgbm__num_leaves': 42, 'lgbm__reg_alpha': 0.09328502944301792, 'lgbm__reg_lambda': 0.4462794992449889, 'lgbm__subsample': 0.9078684483831302} Mejor puntuación AUC-ROC: 0.9989583333333334

En el archivo excel de este repositorio se encuentra el documento denominado "df_results_sorted.xlsx", el cual contiene el total de modelos generados con optimización de hiperparámetros, un total de 1,651 modelos optimizados a partir de los siguientes modelos de algoritmos:
1. Naive Bayes
2. LDA
3. Regresión logística
4. SVM
5. Árboles de decisión
6. Random Forest
7. QDA
8. AdaBoost
9. Gradient Boosting
10. XGBoost
11. LGBM
