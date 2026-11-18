# Actividad 8 - Monitoreo, Gobernanza y Observabilidad de Modelos de Machine Learning

## Descripción

Este proyecto documenta la implementación de una estrategia de monitoreo, observabilidad y gobernanza operativa para un modelo de Machine Learning en producción. El caso de estudio consiste en un modelo de clasificación de aprobación de créditos desarrollado con Random Forest, utilizando MLflow para el registro de métricas, monitoreo y seguimiento del desempeño. 【1-89c217】【2-a781c7】

El objetivo principal es demostrar la aplicación de prácticas modernas de observabilidad, detección de incidentes, monitoreo de rendimiento y respuesta automatizada para garantizar la continuidad y confiabilidad del servicio de Inteligencia Artificial. 【1-89c217】【2-a781c7】

## Objetivos

- Monitorear el desempeño de un modelo de Machine Learning en producción.
- Implementar métricas, logs y trazas para mejorar la observabilidad.
- Definir Alertas Inteligentes basadas en SLOs.
- Detectar condiciones de degradación del modelo y Data Drift.
- Diseñar dashboards para supervisión operativa.
- Documentar runbooks y respuestas automatizadas ante incidentes. 【2-a781c7】

## Tecnologías Utilizadas

- Python
- Scikit-Learn
- Random Forest Classifier
- MLflow
- Pandas
- NumPy
- Matplotlib

## Arquitectura General

1. Generación de datos simulados para solicitudes de crédito.
2. Entrenamiento de un modelo Random Forest.
3. Registro de métricas mediante MLflow.
4. Simulación de alertas e incidentes.
5. Visualización de métricas mediante dashboards.
6. Aplicación de estrategias de monitoreo y gobernanza. 【1-89c217】【2-a781c7】

## Métricas Monitoreadas

### Métricas del Modelo

| Métrica | Objetivo |
|----------|----------|
| Accuracy | > 90% |
| Precision | > 88% |
| Recall | > 85% |
| F1-Score | > 86% |
| Error Rate | < 10% |

### Métricas Operativas

| Métrica | Objetivo |
|----------|----------|
| Latencia Promedio | < 500 ms |
| Latencia P95 | < 800 ms |
| Throughput | > 1000 solicitudes/minuto |
| Disponibilidad | 99.9% |
| Uso de CPU | < 80% |
| Uso de Memoria | < 85% | 【2-a781c7】

## Resultados del Modelo

Durante la evaluación se obtuvieron los siguientes resultados:

| Métrica | Resultado |
|----------|----------|
| Accuracy | 92.10% |
| Precision | 92.64% |
| Recall | 91.33% |
| F1 Score | 91.98% |

Estos resultados demuestran un desempeño estable y consistente para el escenario simulado. 【1-89c217】

## Alertas Configuradas

| Alerta | Condición | Prioridad |
|----------|----------|----------|
| Degradación del Modelo | Accuracy < 85% | Alta |
| Latencia Elevada | Latencia > 800 ms | Media |
| Uso Excesivo de CPU | CPU > 80% | Media |
| Data Drift | PSI > 0.25 | Alta | 【2-a781c7】

## Estrategia de Data Drift

Se utiliza el indicador **Population Stability Index (PSI)** para detectar cambios en la distribución de los datos.

| Valor PSI | Interpretación |
|------------|---------------|
| < 0.1 | Sin cambios relevantes |
| 0.1 - 0.25 | Cambio moderado |
| > 0.25 | Data Drift significativo | 【2-a781c7】

## Incidentes Simulados

### Degradación del Modelo

Se simuló una reducción del Accuracy por debajo del umbral definido para validar el correcto funcionamiento del sistema de alertamiento. 【1-89c217】【2-a781c7】

### Data Drift

Se simuló un PSI de 0.28 para representar cambios significativos entre los datos de entrenamiento y producción. 【1-89c217】【2-a781c7】

## Dashboards

Se diseñaron dashboards para monitorear:

- Rendimiento del modelo.
- Disponibilidad del servicio.
- Latencia.
- Consumo de recursos.
- Detección de Data Drift. 【2-a781c7】

## Respuestas Automatizadas

| Evento Detectado | Acción Automática |
|------------------|------------------|
| Accuracy < 85% | Rollback del modelo |
| PSI > 0.25 | Reentrenamiento |
| CPU > 80% | Escalamiento automático |
| Latencia > 800 ms | Generación de alerta y escalamiento | 【2-a781c7】

## Evidencias

La implementación incluye evidencia visual del proceso completo:

- Instalación de MLflow.
- Generación de datos simulados.
- Entrenamiento del modelo.
- Simulación de alertas.
- Detección de Data Drift.
- Dashboard de monitoreo.

![EMBEDDEDIMAGE](placeholder-0)
![EMBEDDEDIMAGE](placeholder-1)
![EMBEDDEDIMAGE](placeholder-2)

## Autor

**Gibran Martínez Figueroa**

Maestría en Inteligencia Artificial  
Universidad Tecmilenio

## Documentación

- Documento Técnico: GPIA_Actividad_8_DOC_TEC.pdf 【2-a781c7】
- Evidencia de Implementación: GPIA_Actividad_8_IMPLEMENTACION.pdf 【1-89c217】

## Conclusión

La implementación demuestra cómo las prácticas de monitoreo, observabilidad y gobernanza permiten supervisar modelos de Machine Learning en producción, facilitando la detección temprana de incidentes, la aplicación de acciones correctivas y el mantenimiento continuo de la calidad del servicio. 【1-89c217】【2-a781c7】
