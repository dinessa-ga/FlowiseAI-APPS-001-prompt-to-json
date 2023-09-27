# De prompt a JSON

## Índice


- [1. Consideraciones generales](#1-consideraciones-generales)
- [2. Preámbulo](#2-preámbulo)
- [3. Resumen del proyecto](#3-resumen-del-proyecto)
- [4. Objetivos de aprendizaje](#4-objetivos-de-aprendizaje)
- [5. Criterios de aceptación](#5-criterios-de-aceptación)
- [6. Getting started](#6-getting-started)
- [7. Valida tu solución](#7-valida-tu-solución)
- [8. Recursos](#8-recursos)

---

## 1. Consideraciones generales

- Este proyecto lo resolvemos de manera **individual**.
- El rango de tiempo estimado para completar el proyecto es de 1 a 2 Sprints.

## 2. Preámbulo

La Inteligencia Artificial Generativa (IA Generativa) es una rama de la IA que
se centra en crear sistemas capaces de generar contenido nuevo y original, como
imágenes, música o texto, imitando patrones y estilos previamente aprendidos.
Esto puede ser muy útil para automatizar procesos como el generar copys,
escribir email, analizar datos, etc.

Para poder explotar estas capacidades tenemos que hacer uso del “Prompt
Engineering”, la ingeniería de promping es el proceso de diseñar y perfeccionar
cuidadosamente las instrucciones o "prompts" que se utilizan para interactuar
con un modelo de lenguaje AI como GPT-3.5. Implica experimentar con diferentes
preguntas o comandos para obtener respuestas más precisas y útiles del modelo.
La idea es encontrar la forma óptima de expresar una solicitud o consulta para
obtener la respuesta deseada, ajustando la estructura, el tono y el formato del
prompt para maximizar la efectividad de la comunicación con la IA.

## 3. Resumen del proyecto

Aplicarás tus habilidades de prompting para crear una aplicación que aproveche
el encadenamiento de prompts para producir un resultado en formato JSON, tu
chatflow debe tomar el input del usurario y utilizarlo como parte de los prompts
que crearás para generear información extra que le sea útil al usuario,
utilizarás la herramienta [Flowise](https://flowiseai.com/).

El tema y la utilidad de tu aplicación es libre, piensa en un escenario dónde
una usuaria puede aprovechar esta funcionalidad.

En este ejemplo se toma el nombre de un platillo gastronómico y a través de
prompting se obtiene los ingredientes que lo conforman y el país de origen del
platillo, dando esta información como un objeto en formato JSON.

![image](https://github.com/Laboratoria/curriculum/assets/5282075/801b660d-6c92-44ed-9735-0d401f5a3918)

## 4. Objetivos de aprendizaje

Familiarizarse con los principales conceptos alrededor de la
[Inteligencia Artificial Generativa](https://es.wikipedia.org/wiki/Inteligencia_artificial_generativa)
y trabajar con [Flowise](https://docs.flowiseai.com/) para implementar
soluciones AI expuestas atraves de una API.
Flowise es una herramienta basada en [LangChain](https://docs.langchain.com/docs/),
por lo que además deberás poder entender los conceptos fundamentales de esta
herramienta.

- [ ] [Flowise basics](https://www.youtube.com/watch?v=tD6fwQyUIJE&list=PL4HikwTaYE0HDOuXMm5sU6DH6_ZrHBLSJ)
- [ ] [Langchain Components](https://docs.langchain.com/docs/category/components)
- [ ] [Chat models](https://docs.flowiseai.com/chat-models)
- [ ] [Estructuración de Datos](https://learnprompting.org/es/docs/basic_applications/table_generation)
- [ ] [Cadenas](https://docs.langchain.com/docs/components/chains/)
- [ ] [Prompts Templates](https://docs.langchain.com/docs/components/prompts/)

## 5. Criterios de aceptación

1. Deberás configurar tu chatflow de manera que tome el input del usuario y sea
  utilizado como parte de la cadena de prompts.

2. Utilizar el módelo `gpt-3.5-turbo`.

3. El chatbot generado debe ser capaz de generar respuestas en formato JSON.

4. Tus github actions deben pasar exitosamente.

5. Debes utilizar al menos lo siguientes nodos:

- LLM Chain
- Prompt Template
- Chat Prompt Template

## 6. Getting started

### Instalar Flowise

Seguir las indicaciones para instalar globalmente [flowise](https://github.com/FlowiseAI/Flowise)

```bash
npm  install  -g  flowise

npx  flowise  start
```

## 7. Valida tu solución

Necesitarás definir una variable de ambiente con el nombre `OPENAI_API_KEY` y
darle el valor de api key de OpenAI que utilizarás

Antes de ejecutar los test copiar en la carpeta `/test` con el nombre
`'flow.json'` el archivo de exportación del flow implementado

```bash
OPENAI_API_KEY=<TODO:  poner  tu api  key> npm  test
```

Una vez inicializada la herramienta podrás acceder [aquí](http://localhost:3000/)

Utilizarás esta herramienta para crear y configurar tu propia aplicación AI,
la cual podrás utilizar por medio de la UI proporcionada y también a través de
peticiones HTTP.

## 8. Recursos

- [Serie de tutoriales en youtube (inglés)](https://www.youtube.com/watch?v=tD6fwQyUIJE&list=PL4HikwTaYE0HDOuXMm5sU6DH6_ZrHBLSJ)
- [Introducción a Ingenieria de Prompting](https://learnprompting.org/es/docs/basics/prompting)
- [Encadenamiento de Prompts](https://botpress.com/es/blog/what-is-ai-prompt-chaining#:~:text=Permite%20crear%20respuestas%20personalizadas%20basadas,mejora%20el%20compromiso%20del%20usuario.)
