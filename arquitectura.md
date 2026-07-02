---
title: Arquitectura de Red
layout: default
nav_order: 2
---

# Arquitectura de Red y Servidores

El sistema opera mediante comunicación HTTP REST, separando la interfaz de usuario del procesamiento pesado.

## Componentes del Sistema

* **Frontend (Meta Quest 3):** Ejecuta la aplicación compilada en Unity. Captura el audio y lo envía por la red Wi-Fi.
* **Servidor 1 (Enrutador):** Script Flask ejecutándose en el puerto 5050. Recibe el audio, realiza conversión de formato y almacena las trayectorias para el Gemelo Digital.
* **Servidor 2 (Procesamiento):** Script Flask ejecutándose en el puerto 5000. Gestiona los modelos LLM, visión computacional y envía instrucciones por Ethernet al puerto 30002 del UR3.

![Diagrama de Arquitectura](assets/arquitectura.png)
