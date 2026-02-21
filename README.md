# 📊 European Offensive Efficiency Analysis

Análisis de eficiencia ofensiva y poder competitivo en las 5 grandes ligas europeas (2012–2025)

## 🎯 Objetivo del Proyecto

En el fútbol de élite, el volumen ofensivo (tiros, posesión) suele asociarse al poder financiero y estructural de los clubes.
El objetivo de este proyecto no es predecir resultados, sino analizar si la eficiencia ofensiva es una dimensión de rendimiento independiente del poder competitivo (Elo).

Este análisis busca separar:

La capacidad de generar oportunidades (volumen) de la capacidad de convertirlas en goles (eficiencia) y evaluar si clubes con menor jerarquía institucional pueden cerrar brechas competitivas mediante optimización ofensiva.

## ⚙️ Metodología y Diseño Analítico

### 1. Integridad y Calidad de Datos
* Datos públicos a nivel de partido.
* Top 5 ligas europeas: Premier League, La Liga, Bundesliga, Serie A y Ligue 1.
* Periodo de análisis: 2012–2025.

Se aplicó un corte temporal post-2012 tras un análisis exhaustivo de valores nulos y consistencia táctica, asegurando comparabilidad moderna.

**Resultado:** Dataset limpio, sin registros incompletos ni outliers espurios derivados de errores de captura.

### 2. Proxy de Poder Competitivo
Se utilizó el Rating Elo por partido como proxy de jerarquía institucional y poder estructural del equipo.

Justificación: Elo captura rendimiento histórico ajustado por calidad del rival, evitando sesgos de clasificación o puntos aislados.

### 3. Feature Engineering – Métricas de Eficiencia
Se construyeron métricas específicas para aislar calidad ofensiva del volumen bruto:

`Conversion Rate` = Goles / Tiros Totales
`Shot Accuracy` = Tiros a Puerta / Tiros Totales
`Target Conversion Rate` = Goles / Tiros a Puerta

Estas métricas permiten evaluar toma de decisiones ofensiva y calidad de finalización, independientemente de cuántas veces se llegue al área.

4. Exploratory Data Analysis (EDA)

El análisis incluyó:

Distribuciones globales y benchmarks de eficiencia.

Comparativas por liga (medianas, dispersión y rangos inferiores).

Análisis de correlación entre:

Elo y volumen ofensivo

Elo y métricas de eficiencia

Evolución temporal de la eficiencia ofensiva (2012–2025).

Identificación de outliers positivos (clubes altamente eficientes con bajo volumen).

📊 Hallazgos Clave

Elo ↔ Volumen ofensivo: correlación moderada (r ≈ 0.28).
→ El poder competitivo facilita generar oportunidades.

Elo ↔ Conversion Rate: correlación casi nula (r ≈ 0.11).
→ La eficiencia ofensiva es prácticamente independiente del poder estructural.

La eficiencia está estandarizada en el fútbol élite europeo: las diferencias entre ligas son pequeñas, pero el suelo competitivo varía.

Bundesliga: mayor mediana y menor dispersión inferior → mayor exigencia estructural de eficiencia.

Serie A: bajo volumen, alta precisión.

Premier League: alto volumen con eficiencia más volátil.

Se identificaron casos de optimización extrema (ej. Heidenheim, Nottingham Forest), demostrando que la eficiencia puede compensar limitaciones presupuestales.

🧭 Modelo de Cuadrantes (Aplicación Práctica)

A partir de los datos se construyó un marco táctico para clasificar perfiles ofensivos:

Alto Volumen / Alta Eficiencia: Dominancia total.

Bajo Volumen / Alta Eficiencia: Sharpshooters (optimización táctica).

Alto Volumen / Baja Eficiencia: Zona de frustración (problemas de decisión).

Bajo Volumen / Baja Eficiencia: Riesgo competitivo.

Este modelo permite diagnóstico ofensivo accionable para análisis táctico y scouting.

🛠️ Stack Tecnológico

Lenguaje: Python

Data Processing: Pandas, NumPy

Análisis Estadístico: SciPy

Visualización: Matplotlib, Seaborn

Metodología: EDA, Feature Engineering, Sports Analytics

📄 Entregables

Notebook de análisis exploratorio y estadístico.

Club Report v1.1 (PDF): traducción estratégica de los hallazgos para contexto club-facing.

Desarrollado por:
Dan Bernal | Football Analytics
Data Analyst | Tactical & Performance Analysis
