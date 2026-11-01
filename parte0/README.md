# Full Stack Open - Parte 0: Fundamentos de las Aplicaciones Web

Este directorio contiene las soluciones a los ejercicios de la **Parte 0** del curso **Full Stack Open** de la Universidad de Helsinki.

En este módulo se analiza la arquitectura de las aplicaciones web tradicionales y SPA (Single Page Application), el protocolo HTTP, las peticiones `GET` y `POST`, y la manipulación del DOM mediante JavaScript.

---

## Ejercicios Resueltos

| Ejercicio | Descripción | Solución |
| :--- | :--- | :---: |
| **0.4** | Diagrama de secuencia: Nueva nota (App Tradicional) | [`Diagrama 0.4`](./ejercicio_0.4.md) |
| **0.5** | Diagrama de secuencia: Aplicación de una sola página (SPA) | [`Diagrama 0.5`](./ejercicio_0.5.md) |
| **0.6** | Diagrama de secuencia: Nueva nota en SPA | [`Diagrama 0.6`](./ejercicio_0.6.md) |

---

## Diagramas de Secuencia (Sintaxis Mermaid)

Los diagramas fueron creados utilizando la sintaxis [Mermaid](https://mermaid.js.org/) integrada de forma nativa en GitHub.

### Resumen de flujos analizados:

* **App Tradicional (0.4):** El envío del formulario activa un `POST` que responde con una redirección HTTP 302 hacia `/notes`, obligando al navegador a recargar todo el documento HTML y volver a solicitar los archivos CSS, JS y el dataset JSON.
* **Carga de SPA (0.5):** La carga inicial obtiene el documento HTML de la SPA, el archivo CSS y el script ejecutable JavaScript que finalmente solicita la información de las notas en formato JSON sin refrescar la interfaz.
* **Nueva nota en SPA (0.6):** La creación de una nota envía un `POST` enviando el objeto JSON directamente al servidor. Mediante JavaScript en el navegador, la nota se añade dinámicamente a la lista y se vuelve a renderizar el DOM en tiempo real, devolviendo un estado HTTP `201 Created` sin requerir recargas de página ni redirecciones.

---

## Herramientas Utilizadas

* **Lenguajes:** Markdown, Mermaid.js
* **Red de Inspección:** DevTools del navegador (Network Tab)
* **Control de Versiones:** Git & GitHub