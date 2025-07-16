# Sistema de Recomendación Musical Basado en Emociones / Emotion-Based Music Recommendation System

## Descripción / Description

### Español
Este proyecto implementa un sistema de recomendación musical que utiliza el reconocimiento de emociones faciales mediante visión por computadora. El sistema captura expresiones faciales a través de una cámara web, identifica emociones (Feliz, Triste, Enojado, Neutral) y recomienda canciones basadas en la emoción predominante y un género musical seleccionado por el usuario. La interfaz gráfica está desarrollada con PyQt5, y utiliza modelos de machine learning preentrenados para la detección de emociones y la recomendación musical.

### English
This project implements a music recommendation system that uses facial emotion recognition through computer vision. The system captures facial expressions via a webcam, identifies emotions (Happy, Sad, Angry, Neutral), and recommends songs based on the predominant emotion and a user-selected music genre. The graphical interface is developed with PyQt5, and it uses pretrained machine learning models for emotion detection and music recommendation.

---

## Requisitos / Requirements

### Español
Para ejecutar este proyecto, necesitas instalar las siguientes dependencias y tener los archivos necesarios:

1. **Python 3.8 o superior**
2. **Librerías de Python**:
   ```bash
   pip install opencv-python mediapipe numpy pandas joblib PyQt5 matplotlib
   ```
3. **Archivos necesarios**:
   - Modelos preentrenados y escaladores:
     - `FaceRecognition/modelo_knn_mejorado.pkl`
     - `FaceRecognition/scaler.pkl`
     - `FaceRecognition/label_encoder.pkl`
     - `MusicRecomendator/multi_knn_classifiers.pkl`
     - `MusicRecomendator/scaler.pkl`
   - Dataset: `MusicRecomendator/dataset_processed_with_emotions.csv`
   - Imágenes para la página de instrucciones (opcional):
     - `neutral.png`
     - `happy.webp`
     - `angry.webp`
     - `sad.webp`
   - GIF para la página de inicio: `cat-jam-rainbow.gif`
4. **Hardware**:
   - Una cámara web funcional para la detección facial.
   - Recomendable un ambiente bien iluminado para una mejor detección.

### English
To run this project, you need to install the following dependencies and have the required files:

1. **Python 3.8 or higher**
2. **Python Libraries**:
   ```bash
   pip install opencv-python mediapipe numpy pandas joblib PyQt5 matplotlib
   ```
3. **Required Files**:
   - Pretrained models and scalers:
     - `FaceRecognition/modelo_knn_mejorado.pkl`
     - `FaceRecognition/scaler.pkl`
     - `FaceRecognition/label_encoder.pkl`
     - `MusicRecomendator/multi_knn_classifiers.pkl`
     - `MusicRecomendator/scaler.pkl`
   - Dataset: `MusicRecomendator/dataset_processed_with_emotions.csv`
   - Images for the instruction page (optional):
     - `neutral.png`
     - `happy.webp`
     - `angry.webp`
     - `sad.webp`
   - GIF for the start page: `cat-jam-rainbow.gif`
4. **Hardware**:
   - A functional webcam for facial detection.
   - A well-lit environment is recommended for better detection.

---

## Instrucciones de Uso / Usage Instructions

### Español
1. **Configuración del entorno**:
   - Instala las dependencias mencionadas usando `pip`.
   - Asegúrate de que los archivos de modelos, el dataset y las imágenes estén en las rutas especificadas (`FaceRecognition/` y `MusicRecomendator/`).
2. **Ejecución del programa**:
   - Guarda el archivo principal como `FINAL.py`.
   - Ejecuta el script con:
     ```bash
     python FINAL.py
     ```
3. **Interacción con la interfaz**:
   - **Página de inicio**: Haz clic en "Iniciar" para continuar.
   - **Página de instrucciones**: Lee las consideraciones y ejemplos de expresiones faciales, luego haz clic en "Comenzar Detección".
   - **Detección de emociones**: Durante 20 segundos, el sistema capturará tus expresiones faciales. Mantén el rostro frente a la cámara en un ambiente bien iluminado.
   - **Resultados**: Visualiza un gráfico con la distribución de emociones detectadas.
   - **Selección de género**: Elige una categoría musical y un subgénero, luego haz clic en "Generar Recomendación" para obtener una lista de canciones recomendadas.
   - **Satisfacción**: Responde una encuesta de satisfacción (escala de 1 a 10). Los resultados se guardan en `ResultadosRecomendacion.csv`.
4. **Finalización**: Haz clic en "Finalizar" para cerrar la aplicación.

### English
1. **Environment Setup**:
   - Install the required dependencies using `pip`.
   - Ensure the model files, dataset, and images are in the specified paths (`FaceRecognition/` and `MusicRecomendator/`).
2. **Running the Program**:
   - Save the main file as `FINAL.py`.
   - Run the script with:
     ```bash
     python FINAL.py
     ```
3. **Interacting with the Interface**:
   - **Start Page**: Click "Start" to proceed.
   - **Instruction Page**: Review the considerations and examples of facial expressions, then click "Start Detection".
   - **Emotion Detection**: For 20 seconds, the system will capture your facial expressions. Keep your face in front of the camera in a well-lit environment.
   - **Results**: View a graph showing the distribution of detected emotions.
   - **Genre Selection**: Choose a music category and subgenre, then click "Generate Recommendation" to receive a list of recommended songs.
   - **Satisfaction Survey**: Answer a satisfaction survey (scale of 1 to 10). Results are saved to `ResultadosRecomendacion.csv`.
4. **Termination**: Click "Finish" to close the application.

---

## Estructura del Proyecto / Project Structure

### Español
- **`FINAL.py`**: Script principal que contiene la lógica del sistema, la interfaz gráfica y la integración de los modelos.
- **Modelos y Escaladores**:
  - `FaceRecognition/modelo_knn_mejorado.pkl`: Modelo KNN para detección de emociones.
  - `FaceRecognition/scaler.pkl` y `FaceRecognition/label_encoder.pkl`: Escalador y codificador para las características faciales.
  - `MusicRecomendator/multi_knn_classifiers.pkl` y `MusicRecomendator/scaler.pkl`: Modelos y escalador para la recomendación musical.
- **Dataset**: `MusicRecomendator/dataset_processed_with_emotions.csv`: Datos de canciones con etiquetas de emociones y géneros.
- **Imágenes**: Imágenes y GIF para la interfaz gráfica (opcional).

### English
- **`FINAL.py`**: Main script containing the system logic, graphical interface, and model integration.
- **Models and Scalers**:
  - `FaceRecognition/modelo_knn_mejorado.pkl`: KNN model for emotion detection.
  - `FaceRecognition/scaler.pkl` and `FaceRecognition/label_encoder.pkl`: Scaler and label encoder for facial features.
  - `MusicRecomendator/multi_knn_classifiers.pkl` and `MusicRecomendator/scaler.pkl`: Models and scaler for music recommendation.
- **Dataset**: `MusicRecomendator/dataset_processed_with_emotions.csv`: Song data with emotion and genre labels.
- **Images**: Images and GIF for the graphical interface (optional).

---

## Notas Adicionales / Additional Notes

### Español
- Asegúrate de que la cámara web esté funcionando correctamente antes de iniciar.
- Si las imágenes (`neutral.png`, `happy.webp`, etc.) no están disponibles, el sistema mostrará un texto indicando que no se encontraron.
- Los resultados de la detección y la satisfacción del usuario se guardan en `ResultadosRecomendacion.csv`.
- Si no se detectan emociones, el sistema mostrará una advertencia y no permitirá avanzar a la recomendación.

### English
- Ensure the webcam is functioning properly before starting.
- If the images (`neutral.png`, `happy.webp`, etc.) are not available, the system will display a message indicating they were not found.
- Detection results and user satisfaction are saved to `ResultadosRecomendacion.csv`.
- If no emotions are detected, the system will display a warning and prevent proceeding to recommendations.

---

## Licencia / License
Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.  
This project is licensed under the MIT License. See the `LICENSE` file for details.