# Diseño e Implementación de una Arquitectura Híbrida PAG para la Selección de Personal

Este repositorio contiene el código fuente del Trabajo de Fin de Máster (TFM) que diseña, implementa y valida un ecosistema de **Generación Aumentada por Psicometría (PAG)**. 

El proyecto disocia el cálculo matemático de la personalidad (utilizando un modelo local *Fine-Tuned* basado en RoBERTa) de la generación lingüística (utilizando LLMs comerciales como Llama 3.3 a través de Groq) para evadir el sesgo de positividad y las censuras corporativas (RLHF) en procesos de selección de personal B2B.

## 🚀 Estructura del Proyecto

* **`01_Preparacion_Datos.ipynb`**: Descarga, limpieza y Análisis Exploratorio de Datos (EDA) del corpus psicométrico *SenticNet Essays*. Incluye el *Zero-Shot Benchmark* contra Gemini 2.5, Llama 3.3 y Command-R Plus.
* **`02_Fine_Tuning_Modelo.ipynb`**: Entrenamiento especializado de clasificadores multietiqueta (DistilBERT y RoBERTa-base) para la extracción de tensores continuos en el espacio dimensional Big Five ($\mathbb{R}^5$).
* **`03_Sistema_Recomendacion_RRHH.ipynb`**: Implementación del motor matemático mediante Similitud del Coseno, cálculo de deltas y orquestación del flujo agéntico en la nube para la generación automatizada de entrevistas conductuales.

## 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 3
* **Deep Learning:** PyTorch, Hugging Face (Transformers, Datasets)
* **Modelos Locales:** RoBERTa, DistilBERT
* **Inferencia Cloud:** Groq (Llama 3.3 70B), Google GenAI, Cohere
* **Cálculo Científico:** SciPy, Scikit-Learn, Pandas

## ⚙️ Cómo ejecutar el proyecto

1. Clona el repositorio.
2. Instala las dependencias: `pip install -r requirements.txt`.
3. Ejecuta los cuadernos en orden secuencial (se recomienda el uso de Google Colab con GPU T4 para la fase 02 de Fine-Tuning).
4. El sistema solicitará tus propias API Keys de Groq, Gemini y Cohere durante la ejecución. No se incluyen por seguridad.
