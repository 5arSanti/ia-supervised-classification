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

Regla de oro: si alguien que nunca vio el código lo lee, debe entender qué hace cada línea. Los comentarios son parte de la calificación.

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

