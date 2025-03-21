## Repositorio 1: LangChain LLM Chain Tutorial


# LangChain LLM Chain Tutorial

Este repositorio contiene el código y la documentación para una implementación básica utilizando LangChain y la técnica LLM Chain, basada en el [tutorial oficial de LangChain](https://python.langchain.com/docs/tutorials/llm_chain/).
Tambien contine todo la implemnetacion de ejemplo del RAG

## Visión General

Este proyecto tiene como objetivo demostrar los conceptos básicos de LangChain mediante la creación de una cadena que utiliza un modelo de lenguaje (LLM) para generar respuestas a partir de una plantilla predefinida. Se emplea un **PromptTemplate** para transformar la entrada del usuario en mensajes formateados que se pasan al modelo de lenguaje de OpenAI.

## Arquitectura y Componentes

- **LangChain:** Framework para la integración y orquestación de modelos de lenguaje.
- **PromptTemplate:** Componente que permite formatear la entrada del usuario en mensajes estructurados.
- **LLMChain:** Encadena el modelo de lenguaje y el prompt, facilitando la ejecución de la generación de texto.
- **OpenAI:** Proveedor del modelo de lenguaje utilizado.
- **Módulo de Recuperación:** Conecta con Pinecone para buscar documentos relevantes a partir de embeddings.
- **Módulo de Generación:** Utiliza OpenAI para generar respuestas a partir de la información recuperada.
- **RAG Chain:** Combina ambos módulos para formar una cadena de procesamiento que primero recupera información y luego la utiliza para generar respuestas contextualizadas.
- **Integración con LangChain:** Uso de componentes como `RetrievalQA` para facilitar la creación de la cadena RAG.

La aplicación principal se encuentra en el archivo `llm_chain_example.py`, que demuestra la creación y ejecución de la cadena.

## Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu_usuario/llm-chain-tutorial.git
   cd llm-chain-tutorial
   ```

2. Crea y activa un entorno virtual:
   ```bash
   python -m venv env
   ```
   O en pycharm crea el entorno virtual

3. Instala las dependencias:
   ```bash
   pip install langchain
   pip install -qU "langchain[openai]"
   pip install --quiet --upgrade langchain-text-splitters langchain-community langgraph
   pip install -qU langchain-core
   pip install python-dotenv

   ```
   > **Nota:** Crea un archivo .env para todas la variables de entorno para correr el codigo.

## Ejecución del Código

Este codigo poee dos partes la implementacion del LLM que se ejecuta:

```bash
python helloai.py
```
Ahora para ejecutar el RAG se usa:
```bash
python RagPaso.py
```
Es importante tener en cuenta que antes de todo se debe crear el .env para las variables de entorno

## Screenshots de pruebas
# LLM
![image](https://github.com/user-attachments/assets/9bec6db8-f944-4ce6-b56e-cc6f8e329750)
![image](https://github.com/user-attachments/assets/dda6152b-eda7-48c4-99dd-2523c8271a26)
# RAG

INDEXACION
![image](https://github.com/user-attachments/assets/25c895d8-e790-4796-9aae-8b47922c0e7f)

DIVISION

![image](https://github.com/user-attachments/assets/d28b6b90-e6d4-4e82-83fb-3d29e49e7cc8)

ALMACENAMIENTO
![image](https://github.com/user-attachments/assets/c8c35f81-c06a-4f84-9a72-fd3d1682a68a)

RECUPERACION
![image](https://github.com/user-attachments/assets/3c6b8f13-7863-44cc-9a0d-46647adf219b)
![image](https://github.com/user-attachments/assets/31513d1d-d98d-41e8-b730-985b2365101c)




## Documentación Adicional

- [Tutorial de LangChain LLM Chain](https://python.langchain.com/docs/tutorials/llm_chain/)
- [Documentación de LangChain](https://python.langchain.com/)
- [Tutorial Rag](https://python.langchain.com/docs/tutorials/rag/)

## Contribuciones

Las contribuciones son bienvenidas. Siéntete libre de abrir un *issue* o enviar *pull requests* para mejoras o correcciones.

