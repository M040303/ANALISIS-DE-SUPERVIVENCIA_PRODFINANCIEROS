
# Análisis de Supervivencia: Modelación de Cancelación Anticipada (Churn)

Este repositorio contiene el desarrollo de un modelo actuarial para predecir la **cancelación anticipada de contratos** en una institución financiera. El proyecto aplica técnicas de análisis de supervivencia para entender el comportamiento de productos de seguros y ahorro.

## 📊 Resumen del Proyecto
El objetivo es cuantificar el impacto de diversas covariables socioeconómicas en la permanencia de los clientes. Se modela el "tiempo de vida" del contrato (en meses) desde su suscripción hasta el evento de cancelación.

[![Ver Proyecto PDF](https://img.shields.io/badge/Ver_Reporte-PDF-red?style=for-the-badge&logo=adobeacrobatreader)](https://github.com/M040303/ANALISIS-DE-SUPERVIVENCIA_PRODFINANCIEROS/blob/main/BECERRIL_MAURICIO_PROYECTOFINAL.pdf)

### 🛠️ Stack Técnico
- **Lenguaje:** R 4.x
- **Librerías:** `survival`, `survminer`, `ggplot2`, `dplyr`
- **Metodología:** Estimación no paramétrica (Kaplan-Meier) y modelación semiparamétrica (Riesgos Proporcionales de Cox).

## 🧬 Metodología Actuarial

### 1. Análisis no Paramétrico (Kaplan-Meier)
Se utilizaron curvas de supervivencia para comparar la retención entre segmentos. 
* **Hallazgo:** Los productos de **Ahorro** muestran una mayor tasa de supervivencia inicial en comparación con los **Seguros**.

### 2. Ajuste Distribucional
Se validó mediante **PP-plots** que los datos siguen una **Distribución de Weibull**. Esto permite parametrizar la tasa de falla y realizar proyecciones de flujo de efectivo más precisas.

### 3. Modelo de Riesgos Proporcionales de Cox
Se ajustó un modelo para medir el riesgo relativo (Hazard Ratio) de las siguientes variables:
* **Edad y Antigüedad:** Factores protectores que reducen el riesgo de cancelación.
* **Nivel Educativo:** Se identificó que clientes con educación alta tienen un **Hazard Ratio de 1.29**, indicando un mayor riesgo de cancelación bajo condiciones constantes.
* **Ingreso Mensual:** Variable clave para determinar la estabilidad del contrato.





