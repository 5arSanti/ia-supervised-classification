# Construccion paso a paso un modelo de clasificación supervisada

Notebook de Google Colab con los 7 pasos:
•	Celda Markdown con descripción del problema
•	Importacion de librerias comentada
•	Dataset creado o cargado (min. 20 registros)
•	Exploracion visual con minimo 2 graficas
•	Separacion entrenamiento / prueba
•	Entrenamiento e importancia de variables
•	Predicciones y cálculo de accuracy

El notebook debe seguir los 7 pasos en orden. Cada paso en su propia celda, con comentarios que expliquen qué hace el código y por qué.

`Regla de oro: si alguien que nunca vio el código lo lee, debe entender qué hace cada línea. Los comentarios son parte de la calificación.`

1. Celda Markdown — Título y descripción  (5 pts)
Explica con palabras del grupo qué problema van a resolver, cuáles son las variables de entrada y qué quiere predecir el modelo. Mínimo 5 líneas.

2. Importar librerías  (5 pts)
Importa pandas, numpy, matplotlib, seaborn y las funciones de sklearn necesarias. Cada import con comentario que explique para qué sirve en su proyecto específico.

3. Crear o cargar el dataset  (10 pts)
Mínimo 20 registros y 3 variables de entrada. La variable target debe ser categórica (0/1 o similar). Muestra la tabla y cuántos hay de cada categoría.

4. Exploración visual  (10 pts)
Mínimo 2 gráficas comparando las categorías del target. Agrega una celda Markdown después de cada gráfica explicando qué observa el grupo.

5. Separar datos: entrenamiento y prueba  (5 pts)
Divide en 80% entrenamiento y 20% prueba. Muestra cuántos registros quedaron en cada grupo y explica por qué esta separación es necesaria.

6. Entrenar el modelo e importancia de variables  (5 pts)
DecisionTreeClassifier entrenado. Muestra qué variable fue la más importante y comenta si tiene sentido con el contexto del problema del grupo.

7. Predicciones y evaluación  (5 pts)
Tabla comparando predicción vs respuesta real para los datos de prueba. Calcula el accuracy e interprétalo en una oración en lenguaje sencillo.

## Bitácora de autocontextualización

### Tarea 1 - Auditoría inicial de estructura
- Objetivo: mapear `main.ipynb` contra la rúbrica de 7 pasos.
- Cambios aplicados: se identificó que el notebook actual cubre limpieza y normalización (`df_limpio`) pero aún no implementa explícitamente los 7 pasos de clasificación supervisada.
- Validación rápida: celdas revisadas del índice 0 al 18; no existe bloque formal de modelado con `DecisionTreeClassifier`.
- Siguiente paso: crear target categórico desde `puntaje` y definir variables de entrada para clasificación.

### Tarea 2 - Definición de target y variables
- Objetivo: construir variable objetivo y matriz de entrada para clasificación.
- Cambios aplicados: en `main.ipynb` se creó `target_alto_puntaje` a partir de la mediana de `puntaje`, se excluyeron columnas de fuga (`puntaje`, `nivel`, fechas, `id`) y se construyó `X` con codificación one-hot.
- Validación rápida: se reporta total de registros de modelado, umbral de mediana y distribución de clases del target.
- Siguiente paso: incorporar exploración visual mínima de 2 gráficas y su interpretación en markdown.

### Tarea 3 - Exploración visual y lectura de hallazgos
- Objetivo: cumplir el requisito de mínimo 2 gráficas comparando categorías del target.
- Cambios aplicados: se añadieron dos visualizaciones en `main.ipynb` (distribución global del target y comparación de target por `modalidad`) y una celda markdown explicativa después de cada gráfica.
- Validación rápida: las celdas de interpretación explican comportamiento del balance de clases y utilidad potencial de una variable categórica para el modelo.
- Siguiente paso: separar entrenamiento/prueba (80/20), entrenar árbol de decisión y evaluar accuracy.

### Tarea 4 - Entrenamiento y evaluación supervisada
- Objetivo: implementar los pasos 5, 6 y 7 de la rúbrica.
- Cambios aplicados: se agregó `train_test_split` 80/20 con `stratify`, entrenamiento de `DecisionTreeClassifier`, cálculo de importancia de variables, tabla de comparación real vs predicción, `accuracy`, reporte de clasificación y matriz de confusión.
- Validación rápida: el notebook imprime tamaños de entrenamiento/prueba, top de importancias y métricas finales del modelo.
- Siguiente paso: cerrar autocontextualización, verificar consistencia general y dejar entregable listo para ejecución.

### Tarea 5 - Cierre de autocontextualización híbrida
- Objetivo: mantener lineamientos base y agregar seguimiento incremental de implementación.
- Cambios aplicados: se conservó la rúbrica original y se añadieron entradas por tarea con objetivo, cambios, validación y próximo paso.
- Validación rápida: `CONTEXT.md` ahora permite retomar el trabajo desde cualquier etapa del plan sin perder contexto técnico.
- Siguiente paso: ejecutar todas las celdas del nuevo bloque en `main.ipynb` para registrar resultados definitivos en outputs.
