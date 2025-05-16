# 📚 Sistema de consulta inteligente para documentos económicos

## Autores

- Ángela Sofia Torres
- Juan David Saldaña Rivera
- Laura Pabón
- Darío Montoya
- Lucas Alvarado

## Descripción del Proyecto

Este proyecto implementa un sistema RAG (Retrieval Augmented Generation) que permite la consulta y análisis de documentos en formatos PDF, DOCX, CSV y TXT, utilizando LangChain para la orquestación y Ollama (Llama2) como modelo de lenguaje local.

La aplicación procesa los documentos cargados, genera embeddings con el modelo `intfloat/multilingual-e5-small` y almacena los vectores en FAISS para recuperación rápida. Luego, combina los fragmentos relevantes del texto con prompts personalizados para generar respuestas precisas y citar las fuentes.

## Objetivo del Proyecto

- Desarrollar un asistente IA capaz de responder preguntas basadas en el contenido de documentos proporcionados por el usuario.
- Minimizar la latencia utilizando la API directa de Ollama como opción rápida.
- Ofrecer un flujo end-to-end que incluya:
  1. Carga y preprocesamiento de documentos.
  2. División en fragmentos y vectorización.
  3. Almacenamiento y recuperación de contexto relevante.
  4. Generación de respuestas y citación de fuentes.

## Funcionalidades Principales

- Soporte para formatos: PDF, DOCX, CSV, TXT.
- Balance entre método rápido (API directa de Ollama) y robusto (LangChain RetrievalQA).
- Configuración de prompt personalizable.
- Visualización mediante interfaz web con Gradio.

## Tecnologías Utilizadas

- **Python 3.8+**
- **LangChain**: Para orquestar la carga, vectorización y consulta.
- **Ollama (Llama2)**: Modelo LLM local para generación de texto.
- **FAISS**: Base de datos vectorial para almacenamiento y búsqueda de embeddings.
- **HuggingFace Embeddings (`intfloat/multilingual-e5-small`)**: Para codificación semántica.
- **Gradio**: Interfaz web interactiva.

## Requisitos de Instalación
Asegúrate de contar con Python ≥ 3.8 e instala las dependencias:
pip install -r requirements.txt

**(requisitos mínimos dentro de requirements.txt:)**

- langchain  
- langchain_community  
- sentence-transformers  
- pypdf  
- python-docx  
- docx2txt  
- unstructured  
- faiss-cpu  
- gradio  
- ollama  
- datasets  
- requests  

## Instalación
- Clona el repositorio:
  
  1. git clone: https://github.com/tu-usuario/rag-assistant-ollama.git  
  2. cd rag-assistant-ollama
- Configura Ollama:
  1. curl -fsSL https://ollama.com/install.sh | sh  
  2. nohup ollama serve > ollama.log 2>&1 &  
  3. ollama pull llama2  
- Instala dependencias de Python:
  1. pip install -r requirements.txt  

## Uso
1. Ejecuta la aplicación:
   python app.py o el script que lanza Gradio  
2. Abre en el navegador: http://localhost:7860  
3. Carga documentos (PDF, DOCX, CSV, TXT).  
4. Elige método rápido (API Ollama) o estándar (LangChain).  
5. Escribe tu pregunta y recibe respuesta con citas de fuentes.  

## Estructura del Proyecto
    app.py                  # Lanza Gradio  
    requirements.txt        # Dependencias  
    README.md               # Documentación  
    rag_system.py           # Clases RAGSystem y DocumentLoader  
    utils/                  # Módulos auxiliares  

## Contribuciones
- Ángela Sofia Torres (Desarrollo de la presentación a exponer).
- Juan David Saldaña Rivera (Búsqueda de bases y realización de Readme).
- Laura Pabón (Realización de código).
- Darío Montoya (Revisión de código y desarrollo de presentación).
- Lucas Alvarado (Realización de código)

## Relatoría

Durante la clase del 14 de Mayo, Laura, Juan David, Lucas y Dario hicieron la revisión del adelanto de código que había realizado Laura previamente. Asimismo, Juan David continuaría con la búsqueda de más bases de datos debido a que existían problemas con las bases de aquel momento. Por su parte, Lucas, Dario y Laura continuarían con la revisión de código. Durante la clase, se definieron los roles a seguir para el resto del proyecto, que son los que se mencionaron anteriormente en el apartado de contribuciones. El jueves 15 de Mayo, los encargados de la realización de código (Laura, Lucas y Dario) continuaron con su trabajo, mientras que Sofía realizaba la presentación y Juan David complementaba el Readme de acuerdo a los ajustes de código. Finalmente, cada uno contribuyó con su parte con los plazos de entrega asignados por los grupos siendo un trabajo satisfactorio.

## Licencia
Licencia MIT — consulta el archivo LICENSE para detalles.








