# Predicciones de ventas
Este proyecto es una actividad a ser realizada como parte de la formación académica dentro del Bootcamp Data Science de Coding Dojo, cuya finalidad es integrar los conocimientos adquiridos en el curso mediante la resolución de un problema que se desarrollará en forma transversal en cada módulo del programa.

El proyecto en cuestión consiste en la predicción de ventas para productos alimenticios, los cuales han sidio venididos en diferentes tiendas. Para ello, se deben aplicar diversas herramientas y ténicas de la Ciencia de Datos, entre otras las siguientes:

- Comprobación de tipos de datos
- Análisis de inconsistencias en los registros
- Detección y tratamiento de valores nulos
- Análisis exploratorio de datos

![Tendencia de Ventas](/TendenciaVentas.png "Tendencia de Ventas")


Posterior al análisis exploratorio y al preprocesamiento de datos, se eligen dos modelos para efectuar las predicciones de ventas:

- Regresión lineal
- Árboles de decisión

De este último modelo se somenten a pruebas dos versiones: una con parámetros por defecto y otra donde se optimiza el parámetro
'máxima profundidad' del árbol de decisión

![Gráfico R2 vs Profundidad máxima](/R2vsMaxDepth.png "Gráfico R2 vs Profundidad máxima")

Los resultados de las métricas obtenidas sobre de test set son las siguientes:

| Modelo                                     |    R2    |   RECM   |
|--------------------------------------------|----------|----------|
| Regresión Lineal                           |  0.383   |   1304   |
| Árbol de decisión (parámetros por defecto) |  0.243   |   1444   |
| Árbol de decisión (optimizado)             |  0.596   |   1055   |

En base al desempeño obtenido con 2 métricas de evaluación (R-cuadrado y la Raíz de Error Cuadrático Medio), se recomienda la utilización de un Árbol de decisión con una profundidad máxima de 5 niveles para las predicciones de ventas de productos alimenticios.

![Árbol de decisión optimizado - 5 niveles](/DecisionTreeOptimo.png "Árbol de decisión optimizado")
