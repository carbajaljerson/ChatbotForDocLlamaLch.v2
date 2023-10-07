# Lectura de Multiples Documentos Chatbot con Langchain y Streamlit

<p align=center>
<img src="src\banner.png" height = 450 weight=800>
<p>


## Arquitectura de la aplicación

<p align=center>
<img src="src\arq.png" height = 360 weight=200>
<p>

- Carga de los documentos 
- Extracción del contenido 
- Se parte el contenido y se divide en segmentos
- Creación de embaddings para cada segmento 
- Construcción de la Semántica para generar la Base de Conocimiento  
- Cuando el usuario genere una pregunta se crean embeddings y una búsqueda semántica para encontrar similitudes en la Base de Conocimiento, luego de obtener las respuestas se clasificarán los resultados entrará al LLM y luego se dará la respuesta al usuario.


## Ejecución Local 💻

Siga estos pasos para configurar y ejecutar el proyecto localmente:

### Pre-requisitos
- Python 3.8 o superior
- Git

### Instalación
Clonar el repositorio :
```bash
git clone https://github.com/carbajaljerson/ChatbotForDocLlamaLch.v2.git
```

Crear el entorno virtual :
```bash
python -m virtualenv env
source env/Scripts/activate
```

Instalar las dependencias en el ambiente virtual :

```bash
pip install -r requirements.txt
```
Modelo cuantizado:

```bash
GIT_LFS_SKIP_SMUDGE=1

wget https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/resolve/main/llama-2-7b-chat.ggmlv3.q4_0.bin

git clone https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2

```


Lanzar el servicio localmente :

```bash
streamlit run app.py
```