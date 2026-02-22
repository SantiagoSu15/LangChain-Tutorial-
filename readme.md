# Introduccion a RAGs con OpeanAI y LangChain

Este proyecto demuestra conceptos basicos de LangChain  utilizando los modelos de lenguaje de OpenAI y LangChain.

Siguiendo el tutorial `https://docs.langchain.com/oss/python/langchain/quickstart`



## Empezando

Estas instrucciones permiten obtener una copia del proyecto en funcionamiento en local para desarrollo y prueba.

### Prerequisitos
```
- Python 3.10 o mayor
- OpenAI API Key
- pip package manager
```

### Instalacion

1. **Clonar el repositorio**

```
    git clone https://github.com/SantiagoSu15/LangChain-Tutorial-.git
```
2. **Crear un entorno virtual**

```
    py -m venv venv
```

3. **Activar el entorno virtual**

```bash
    venv\Scripts\activate
```

4. **Instalar Dependencias**

```bash
    pip install -r requirements.txt
```

5. **Instalar Dependencias**

```bash
    set OPENAI_API_KEY=your_openai_key  
```
6. **Ejecutar**

```bash
    python agent.py
```


## Actividad 

 `agent.py` implementa un agente conversacional con memoria usando LangChain. El agente actúa como un pronosticador del tiempo que responde siempre con juegos de palabras.

 **Define dos herramientas (`@tool`)**:
  - `get_weather_for_location`: devuelve el clima para una ciudad dada.
  - `get_user_location`: obtiene la ubicación del usuario a partir de su `user_id` (pasado por contexto en tiempo de ejecución).

- **Inicializa el modelo** `gpt-3.5-turbo` con temperatura y límites de tokens configurados.

- **Define un esquema de respuesta estructurada** (`ResponseFormat`) con dos campos: una respuesta con juego de palabras y las condiciones del clima (opcional).

- **Crea un agente** con `create_agent` que combina el modelo, las herramientas, un prompt de sistema, el esquema de contexto y un checkpointer en memoria para mantener el historial de conversación entre turnos.

- **Ejecuta el agente** en dos turnos de conversación usando el mismo `thread_id`, demostrando que el agente recuerda el contexto de mensajes anteriores.


Nota: todo el codigo se hizo en base al tutorial **LangChain LLM Chain**


## Autor

* **Santiago Suarez**
