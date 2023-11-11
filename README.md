# MLDiabetes
**MLDiabetes**

## Entorno Virtual
Se recomienda utilizar un entorno virtual para aislar las dependencias de este proyecto de otros proyectos Python en tu sistema. Sigue estos pasos para configurar el entorno virtual:

1. Abre una terminal en la ubicación donde clonaste este repositorio.

2. Crea un nuevo entorno virtual:
   ```bash
   python -m venv venv
   ```

3. Activa el entorno virtual:
   - En Windows:
     ```bash
     venv\Scripts\activate
     ```
   - En macOS y Linux:
     ```bash
     source venv/bin/activate
     ```

## ejecutar el proyecto

1. Si tienes un entorno virtual, verifica que este activado

2. Instala las dependencias usando `pip`:
   ```bash
   pip install -r requirements.txt
   ```
3.Ejecuta cada celda de forma secuencial.

## Contenido
1. Importación de datos y exploración básica
En esta sección, se importan los datos del archivo CSV ("diabetes_prediction_dataset.csv") utilizando pandas y se realiza una exploración básica de los datos. Se imprimen las características del conjunto de datos, se muestra un ejemplo de los primeros registros y se visualiza la distribución de las variables a través de gráficos.

2. Tratamiento de Datos: Conversión de Datos Categóricos a Numéricos
En esta etapa, se realiza la conversión de datos categóricos en representaciones numéricas utilizando OneHotEncoder. Se aplican estos encoders a las columnas 'gender' y 'smoking_history'. Además, se genera una matriz de correlación para analizar las relaciones entre las variables, identificando correlaciones fuertes y moderadas.

3. Partición de los datos para entrenamiento
Los datos se dividen en conjuntos de entrenamiento (70%) y prueba (30%) utilizando la función train_test_split de scikit-learn.

4. Uso de la técnica de sobre-muestreo
En esta sección, se aplica la técnica de sobre-muestreo utilizando SMOTENC para abordar el desbalance en la variable objetivo ('diabetes'). Se realiza un análisis gráfico para comparar la distribución de datos antes y después del sobre-muestreo.

5. Entrenamiento y selección de los mejores hiperparámetros de cada modelo
Se utilizan tres modelos de aprendizaje supervisado: Redes Neuronales, Gradient Boosting Tree y SVM. Cada modelo se entrena con diferentes combinaciones de hiperparámetros, y se evalúa su rendimiento utilizando métricas como F1-Score, precisión, sensibilidad, exactitud y especificidad.

      5.1 Redes Neuronales
      Se prueba la arquitectura de la red neuronal variando el número de capas ocultas y el número de neuronas por capa. Se muestra un gráfico que compara el F1-Score en conjunto de entrenamiento, validación        cruzada y prueba para diferentes configuraciones de hiperparámetros.
      
      5.2 Gradient Boosting Tree
      Se evalúa el rendimiento del modelo Gradient Boosting Tree con diferentes cantidades de árboles y variables máximas. Al igual que en las redes neuronales, se muestra un gráfico que compara el F1-Score         en conjunto de entrenamiento, validación cruzada y prueba.
      
      5.3 SVM
      Se ajusta un modelo SVM variando el parámetro de regularización (C) y se evalúa su rendimiento. También se muestra un gráfico que compara las métricas en diferentes valores de C.
      


