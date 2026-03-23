# Seminario 3 — De Píxeles a Significado Compartido

**Sistemas Inteligentes · Universitat Jaume I**

---

## ¿De qué va este seminario?

En los seminarios anteriores aprendisteis a representar **texto** como vectores y a razonar en ese espacio semántico. En este seminario damos el siguiente paso: ¿pueden las **imágenes** vivir en el mismo espacio que las palabras?

La respuesta es sí, y el modelo que lo hace posible se llama **CLIP**. Con él podréis comparar directamente una foto y una frase usando la misma similitud coseno que ya conocéis. Eso permite cosas como clasificar imágenes sin entrenar nada, buscar fotos con texto, o encontrar objetos en una imagen describiendo lo que buscas.

---

## ¿Qué aprenderéis?

- Cómo un ordenador representa una imagen (píxeles → patches → embeddings)
- Qué es la *patchification* y por qué es la analogía visual de la tokenización
- Cómo CLIP proyecta texto e imagen al mismo espacio vectorial
- Zero-shot classification: clasificar sin entrenar
- Búsqueda semántica de imágenes con texto
- Segmentación guiada por lenguaje natural (SAM + SigLIP)

---

## Orden de los notebooks

### Parte 1 — `Colab_Seminario3_Part1.ipynb`

El núcleo del seminario. Cubre todo el pipeline de CLIP:

1. Carga del modelo y preprocesamiento de imágenes
2. Patchification — la tokenización visual
3. Embeddings de imágenes y similitud coseno
4. PCA del espacio visual
5. Espacio compartido texto ↔ imagen
6. Zero-shot classification en Caltech-101
7. Buscador semántico de imágenes

### Parte 2 — `Colab_Seminario3_Part2.ipynb`

Extensión opcional con segmentación guiada por texto. Combina dos modelos:

- **SAM** (Segment Anything Model, Meta): genera automáticamente todas las máscaras posibles de una imagen
- **SigLIP** (Google): compara cada región recortada con un texto query

Resultado: puedes escribir "el mando de videojuegos" y el sistema lo encuentra y resalta en la imagen.

---

## Requisitos

Los notebooks están diseñados para ejecutarse en **Google Colab**. No necesitáis instalar nada localmente — todas las dependencias se instalan en la primera celda. Hay que asegurarse de usar el colab con GPU.
