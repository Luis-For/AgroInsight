# 🌱 data-processing-service

**Módulo de Procesamiento de Datos para AgroInsight**  
Tecnología: Python  
Responsable de: Limpieza, transformación y normalización de datos agrícolas.

---

## 📌 Descripción

Este microservicio es parte de la plataforma **AgroInsight**, y su objetivo principal es procesar los datos crudos recibidos desde el módulo de ingesta (`data-ingestion-service`) para dejarlos listos para el análisis avanzado, visualización y generación de reportes.

---

## 🎯 Funcionalidades clave

- **Limpieza de datos**  
  - Eliminación de valores nulos, duplicados o inconsistentes.  
  - Conversión de tipos de datos (por ejemplo: cadenas a fechas, números a flotantes).  
  - Validación de rangos o unidades (ej: temperatura, humedad, etc.).

- **Transformación de datos**  
  - Agrupamiento por fechas, zonas geográficas o cultivos.  
  - Enriquecimiento con datos externos si es necesario.  
  - Conversión a formatos estándar para otros servicios.

- **Normalización de datos**  
  - Escalado de variables (Min-Max, Z-score, etc.).  
  - Estandarización de nombres de columnas o categorías.  
  - Preparación para modelos de análisis predictivo.

---

## 🔁 Flujo de trabajo

1. Recibe datos crudos desde `data-ingestion-service` (por REST API, mensaje en cola, o archivo CSV).
2. Aplica reglas de limpieza y transformación configurables.
3. Devuelve los datos procesados a una base de datos intermedia o los reenvía al `analytics-service`.

---

## 🛠 Tecnologías y herramientas sugeridas

- **Python** 3.10+
- Librerías: `pandas`, `numpy`, `pydantic`, `fastapi` (o `Flask`)
- Integración con RabbitMQ / Redis para colas (opcional)
- Logging con `loguru` o `logging`

---

## 📂 Estructura del código (sugerida)

