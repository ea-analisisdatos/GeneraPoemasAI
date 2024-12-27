
# GeneraPoemasAI 🤖📝  

## ¡Bienvenido al proyecto GeneraPoemasAI! 

Este proyecto tiene como objetivo generar poesía, cuentos o cualquier otro tipo de texto utilizando modelos de lenguaje preentrenados de Hugging Face.

## Índice 📚  
1.  [Objetivo](#objetivo)  
2.  [Características](#características)  
3.  [Instalación de Librerías Necesarias](#instalación-de-librerías-necesarias)  
4.  [Uso del Código](#uso-del-código)  
5.  [Consideraciones sobre Recursos](#consideraciones-sobre-recursos)  
6.  [Lecciones Aprendidas](#lecciones-aprendidas)  
7.  [Otros Proyectos Posibles](#otros-proyectos-posibles)  
8. [Contacto](#contacto) 

## Objetivo🎯<a name="objetivo"></a>
**Prototipado de Modelos de Lenguaje**: 
- Explorar y probar modelos preentrenados de Hugging Face. 

**Proyecto GeneraPoemasAI**: 
- Generar texto creativo utilizando modelos de lenguaje. 

## Características ✨<a name="características"></a> 
- Utiliza el modelo `microsoft/phi-2` (un modelo causal de lenguaje preentrenado) para:  
- Descargar y guardar un tokenizador y un modelo preentrenado.  
- Cargar estos elementos en memoria para su modificación.  
- Generar texto basado en una entrada específica proporcionada por el usuario. 

## Instalación de Librerías Necesarias 📦<a name="instalación-de-librerías-necesarias"></a>  
### Requisitos Previos  
-  **Entorno de Python**: 
Asegúrate de tener Python instalado en tu sistema. Puedes descargarlo desde [python.org](https://www.python.org/). 

-  **Librerías**: 
Instala las siguientes librerías usando pip:  ```bash
  pip install transformers huggingface_hub torch python-dotenv``

## Uso del Código 💻<a name="uso-del-código"></a>

1.  **Cargar Variables de Entorno**:
    
 -   El código utiliza la biblioteca  `python-dotenv`  para cargar variables de entorno desde un archivo  `.env`  ubicado en Google Drive.
  -   Asegúrate de tener un archivo  `.env`  con tu token de Hugging Face:
        
        `HF_TOKEN=tu_token_de_hugging_face`
        
2.  **Cargar el Modelo y el Tokenizador**:
    
   -   La función  `load_model_and_tokenizer`  carga el modelo y el tokenizador desde Hugging Face, utilizando el directorio de caché para almacenar los archivos descargados.
   
   -   Configura el  `pad_token_id`  si no está establecido y asegura que el modelo y el tokenizador estén alineados.
   
3.  **Generar Texto**:
   -   La función  `generate_text`  utiliza el modelo y el tokenizador para generar texto basado en una entrada específica.
    -   Incluye la  `attention_mask`  para asegurar resultados confiables.
    -   Define el número de tokens generados (`max_new_tokens`) para optimizar el uso de recursos.
    
    -   ***Ejemplo de uso:***
        `input_text =  "Escribe un poema sobre la inteligencia artificial y su impacto en la humanidad."  poem = generate_text(input_text)  print("\nPoema generado:\n", poem)`
        

## Consideraciones sobre Recursos 📊<a name="consideraciones-sobre-recursos"></a>

**Google Colab y Codespaces**: 
- Ambos entornos tienen limitaciones en cuanto a recursos cuando se utilizan con licencias gratuitas. Por esta razón, el código incluye funciones para liberar memoria y eliminar archivos de caché después de su uso.

**Liberar Memoria**: 
- La función  `clear_cache_directory`  elimina los archivos del modelo del directorio de caché para liberar espacio.

**Número de Tokens**: 
- Ajusta el valor de  `max_new_tokens`  según tus necesidades y recursos disponibles para evitar problemas de almacenamiento.

## Lecciones Aprendidas 📚<a name="lecciones-aprendidas"></a>

**Manejo de Recursos**: 
- Aprendimos la importancia de liberar memoria y eliminar archivos de caché para optimizar el uso de recursos en entornos con limitaciones.

**Uso de Modelos de Lenguaje**: 
- Exploramos cómo utilizar modelos preentrenados de Hugging Face para generar texto creativo.

**Configuración de Parámetros**: 
- Aprendimos a configurar parámetros importantes como  `pad_token_id`,  `attention_mask`  y  `max_new_tokens`  para obtener resultados confiables.

## Otros Proyectos Posibles 🚀<a name="otros-proyectos-posibles"></a>

-   **Generación de Historias**: Utilizar modelos de lenguaje para generar cuentos o novelas.
-   **Chatbots**: Crear chatbots que puedan mantener conversaciones coherentes.
-   **Resúmenes de Texto**: Generar resúmenes de artículos o documentos largos.
-   **Traducción Automática**: Utilizar modelos multilingües para traducir texto entre diferentes idiomas.

## Contacto 📧<a name="contacto"></a>

Si tienes alguna pregunta o sugerencia, no dudes en contactarme. 

***¡Gracias por visitar mi proyecto!***

> Escrito por [Erika Alvares](https://www.erikaalvares.es/).
