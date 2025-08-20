# 📡 Telecom X – Predicción de Cancelación de Clientes (Churn)

## 📖 Contexto
La retención de clientes es uno de los principales retos para las empresas de telecomunicaciones. El presente proyecto tiene como propósito **construir un modelo predictivo de cancelación (churn)** para **Telecom X**, con el fin de identificar a los usuarios con mayor probabilidad de abandonar el servicio y generar acciones preventivas.

Este trabajo corresponde a la segunda parte del desafío **Telecom X Challenge**, enfocado en **Machine Learning aplicado a clasificación binaria**.

---

## 🎯 Objetivos

- Realizar un **preprocesamiento exhaustivo** de los datos (limpieza, codificación y normalización).
- Desarrollar **nuevas variables derivadas** (ejemplo: `Charges.Daily`).
- Entrenar y evaluar modelos de clasificación, con énfasis en **Random Forest**.
- Medir el rendimiento mediante **métricas de exactitud, ROC AUC y matrices de confusión**.
- Identificar las principales características que influyen en la decisión de cancelar.

---

## 📊 Dataset

El dataset contiene información sobre clientes de Telecom X, incluyendo variables relacionadas con:
- **Datos demográficos** (edad, dependientes, pareja).
- **Servicios contratados** (internet, seguridad en línea, soporte técnico).
- **Condiciones contractuales** (tipo de contrato, método de pago, facturación electrónica).
- **Comportamiento de uso** (tenure, cargos mensuales, cargos totales).
- **Variable objetivo**: `Churn` (0 = cliente permanece, 1 = cliente cancela).

---

## 🛠️ Preparación de los Datos

- Eliminación de columnas sin relevancia para el análisis.
- Recodificación de categorías redundantes (ejemplo: reemplazo de *No Internet Service* por *No*).
- Conversión de variables categóricas en numéricas.
- Creación de nuevas variables como **`Charges.Daily`**, obtenida a partir de cargos mensuales/diarios.

---

## 🤖 Modelado

Se evaluaron distintos modelos de clasificación, destacando el uso de **Random Forest**:

- **Random Forest**
  - Exactitud (Accuracy): `~76%`
  - ROC AUC: `~0.81`
  - Buen desempeño en la clase negativa (clientes que permanecen).
  - Mejora en la detección de clientes en riesgo de cancelar frente a otros modelos básicos.

---

## 📈 Resultados

- La **variable de contrato** (tipo y duración) resultó ser uno de los factores más influyentes en la cancelación.
- Los **cargos mensuales** y el **método de pago** también demostraron gran relevancia.
- El modelo permite identificar clientes con **perfil de alto riesgo**, aunque con margen de mejora en recall para la clase positiva (clientes que cancelan).

---

## 🚀 Conclusiones Estratégicas

- **Contratos de corto plazo** (mes a mes) están fuertemente asociados con la cancelación.
- Los clientes con **cargos altos y servicios adicionales** tienden a presentar mayor churn.
- Métodos de pago electrónicos (ej. *Electronic Check*) se relacionan con mayor riesgo de cancelación.
- El modelo puede ser utilizado como **herramienta predictiva inicial**, que se podrá mejorar con técnicas de optimización y modelos adicionales.

---

## 📌 Tecnologías Utilizadas

- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn (preprocesamiento, Random Forest, métricas)
- Jupyter Notebook

---
