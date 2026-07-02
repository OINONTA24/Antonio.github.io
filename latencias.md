---
title: Latencias y Métricas
layout: default
parent: Evaluación LLM
nav_order: 2
---

# Análisis de Latencia y Rendimiento

A continuación, se detalla el tiempo de ejecución de cada componente del código durante el ciclo completo de procesamiento.

| Fase | Componente de Código | Tiempo (segundos) |
| :--- | :--- | :--- |
| 1 | Whisper (STT) | 0.52 |
| 1 | Groq (Llama-3.3-70b) | 0.48 |
| 2 | OpenAI (Generación de Imagen) | 14.64 |
| 3 | OpenCV (Cálculo de trayectoria) | 0.07 |
| **Total** | **Pipeline Completo** | **16.28** |

## Justificación de la Arquitectura
Aunque la llamada a la API de OpenAI representa el mayor tiempo de espera, esta decisión de diseño en el código es estrictamente necesaria. Priorizamos la precisión en la comprensión semántica de los *prompts* antes de enviar la matriz de coordenadas finales al robot UR3.
