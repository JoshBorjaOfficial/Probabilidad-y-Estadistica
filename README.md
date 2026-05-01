Proyecto de Probabilidad y Estadística - Ing. en Computación
Realizado por: Borja Hernández Joshua

📊 **Sistema de Análisis Estadístico: Latencia de Shaders**
Este repositorio contiene un conjunto de herramientas desarrolladas en lenguaje C para el análisis de rendimiento de subprocesos gráficos (Shaders). El proyecto simula y procesa datos de latencia para obtener un diagnóstico estadístico completo.

📂 **Estructura del Proyecto**
El repositorio se divide en tres programas que representan la evolución del sistema:
1. calculadora_resumen.c (Ingreso Manual)
  •	Descripción: Permite al usuario definir el tamaño de la muestra y capturar los datos uno a uno.
  •	Funcionalidad: Ideal para validar cálculos estadísticos con datos conocidos. Incluye la tabla de varianza completa y cálculo de percentiles con interpolación.
2. generador_aleatorio.c (Simulador de Carga)
  •	Descripción: Genera automáticamente 200 muestras de latencia en un rango de 150 a 1300 us.
  •	Propósito: Probar el comportamiento del sistema ante volúmenes masivos de datos sin necesidad de entrada manual.
3. analizador_final.c (Sistema Integral - Versión Principal)
Este es el programa definitivo que combina la generación aleatoria con un motor de análisis avanzado.
  •	Algoritmo de Ordenamiento: Implementa QuickSort con la técnica de "Mediana de Tres" para garantizar un rendimiento óptimo de O(n log n).
  •	Estadística Descriptiva:
    o	Medidas de tendencia central: Media, Mediana y Moda (Soporta series Multimodales).
    o	Medidas de dispersión: Varianza, Desviación Estándar y Rango.
    o	Posición: Percentiles configurables por el usuario.
  •	Visualización de Datos:
    o	Histograma de Frecuencias: Basado en la Regla de Sturges para la creación de 9 intervalos de clase proporcionales.
    o	Diagrama de Tallo y Hojas: Una representación visual de la densidad de los datos (Tallo en centenas, Hoja en decenas).
   
🛠️ **Especificaciones Técnicas**
Para garantizar la calidad y precisión de los resultados, el sistema utiliza:
  •	Librería math.h: Para el cálculo de raíces cuadradas y potencias en la varianza.
  •	Interpolación Lineal: Para obtener valores precisos en los percentiles cuando la posición no es un entero exacto.
  •	Formateo de Tablas: Uso de especificadores de formato en C (%-10s, %12.2f) para asegurar que los reportes sean legibles y profesionales en la terminal.

