---
title: Pipeline de Inteligencia Artificial
layout: default
nav_order: 3
---

# Modelos de Inteligencia Artificial

El procesamiento de lenguaje y la generación visual ocurren en cuatro fases secuenciales en el backend.

## Fases del código

1. **Reconocimiento de Voz (Whisper):** Transcripción local de audio a texto.
2. **Procesamiento de Lenguaje (Llama-3.3-70b):** Uso de la API de Groq para extraer intenciones y generar un objeto JSON estructurado con nombres y posiciones.
3. **Generación Visual (DALL-E):** Creación de una imagen vectorial simplificada a partir del contexto espacial.
4. **Visión Computacional (OpenCV):** Procesamiento de la imagen, binarización y extracción de contornos usando el algoritmo Douglas-Peucker para obtener coordenadas UV.
