# Clasificación de Tumores Cerebrales con YOLO

Proyecto de clasificación binaria de imágenes MRI cerebrales utilizando arquitecturas YOLO.

El objetivo fue diferenciar entre dos clases:

- `glioma`
- `no_glioma`

Se utilizó el dataset público **Brain Tumor MRI Dataset** de Kaggle, originalmente compuesto por cuatro clases (`glioma`, `meningioma`, `pituitary` y `notumor`). Las tres últimas fueron agrupadas en la clase `no_glioma`.

Se entrenaron y compararon tres modelos de clasificación:

- YOLOv8n-cls
- YOLOv8s-cls
- YOLO11n-cls

El mejor modelo base fue **YOLOv8n-cls**, con una accuracy de test de aproximadamente **95,56%**.

Posteriormente se realizó una etapa de tuning a partir de los pesos `best.pt`, modificando parámetros como el learning rate, tamaño de imagen, batch size y optimizador. El modelo tuned alcanzó una accuracy de test aproximada de **95,94%**.

Además de accuracy, se analizaron métricas como:

- Precision
- Recall
- F1-score
- Balanced Accuracy
- Matriz de confusión

El proyecto fue desarrollado en Google Colab utilizando Claude, Chatgpt, Python, PyTorch y la librería Ultralytics.
