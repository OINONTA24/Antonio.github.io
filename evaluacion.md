---
title: Evaluación y Métricas
layout: default
nav_order: 4
---

# Evaluación de arquitecturas LLM aplicadas: backend y robótica

Esta sección presenta la metodología para evaluar el comportamiento del sistema completo: captura de usuario, interpretación del modelo, generación visual, segmentación de imagen y latencia de red.

## Latencias y Tiempos de Ejecución

El siguiente cuadro detalla el tiempo de ejecución en segundos de cada componente del código.

| Fase | Componente de Código | Tiempo (segundos) |
| :--- | :--- | :--- |
| 1 | Whisper (STT) | 0.52 |
| 1 | Groq (Llama-3.3-70b) | 0.48 |
| 2 | OpenAI (Generación de Imagen) | 14.64 |
| 3 | OpenCV (Cálculo de trayectoria) | 0.07 |
| **Total** | **Pipeline Completo** | **16.28** |

> **Nota de diseño:** La latencia principal recae en el modelo de difusión de imágenes. Esta decisión arquitectónica prioriza la correcta espacialidad y coherencia geométrica de los trazos antes de enviar los waypoints al efector final del robot.
