# Laboratorio 3: evaluar entidades

Orden de ejecución: abrir Laboratorio_03.ipynb dentro del paquete (junto a entidades.json), con kernel nuevo, y correr las celdas de arriba hacia abajo. La última celda de código crea esta carpeta.

Versiones: {"Python": "3.14.4", "spaCy": "3.8.16", "pandas": "3.0.5"}. El curso pide Python 3.11; aquí corrió con la versión indicada.

Datos: entidades.json, sin modificar. Muestra: los primeros cinco textos de test, E10_0, E10_1, E10_2, E10_3, E11_0.

Reglas, definidas antes de medir: spacy.blank('es') con EntityRuler. PRODUCTO es AulaPro, MesaApp o NubeTec (frase exacta). FOLIO es un token que cumple ^INC-\d{4}$. No hay aleatoriedad ni semilla.

Evaluación: coincidencia exacta de (id, inicio, fin, tipo). Si un denominador es cero, la métrica vale 0.

Resultado en los cinco textos: TP=10, FP=0, FN=0, precisión=1.0, recall=1.0, F1=1.0.

Errores: dos simulados sobre copias (límite en E10_0 y tipo en E11_0), cada uno con TP 9, FP 1, FN 1 y métricas de 0.9. El análisis está en el notebook.

Límites: cinco textos de dos familias; un F1 alto aquí no prueba que reconozca productos o folios nuevos.

Archivos: predicciones.csv, metricas.json y este README.
