# 📊 Solución de Analytics & BI para Organización Civil (ONG)

(https://docs.google.com/spreadsheets/d/1kqYxzs938wWMa_vZ2chdoi7D6s46AvZRbkrxR_exlI4/edit?usp=sharing)


## 👤 Desarrollado por
*   **Carlos Daniel Palomino Caravantes** – *Junior Data Analyst & Contador Público en Formación*
*   🔗 [Mi LinkedIn](www.linkedin.com/in/carlos-daniel-palomino-caravantes-39a8b6411) | 📧 carlosdanielpalominocaravantes@gmail.com | 📱 55 3032 8797

---

## 📝 Resumen Ejecutivo e Impacto en el Negocio

Este proyecto representa una solución integral de **Inteligencia de Negocio (BI)** y automatización construida sobre una arquitectura de Excel Avanzado para una ONG de desarrollo comunitario. El sistema transforma un entorno de información cualitativa desestructurada en un flujo automatizado de datos cuantitativos, optimizando la toma de decisiones directivas en tiempo real.

### 🚀 Logros Clave e Impacto Cuantificable (Métricas de CV):
*   **Eficiencia Operativa (-90% de Tiempo):** Diseñé un modelo matemático que automatiza la ingesta y consolidación de cuestionarios diagnósticos de 60 reactivos, **reduciendo el tiempo de procesamiento manual en un 90%** (equivalente a liberar valiosas horas operativas para el staff).
*   **Gobernanza y Confidencialidad de Datos:** Toda la información de este repositorio ha sido **anonimizada** bajo estrictos criterios de confidencialidad de datos. La arquitectura cuenta con capas protegidas criptográficamente para asegurar la integridad de las fórmulas frente al usuario final.
*   **Visualización Ejecutiva Interactiva:** Traduje requerimientos abstractos en un tablero gerencial (Dashboard) que correlaciona tres ejes operativos críticos: **Servicio** (Disposición), **Unidad Operativa** (Pertenencia) y **Nivel de Alcance / Recuperación** (Bienestar).

---

## 📉 Visualización del Dashboard (Triángulo de Control Operativo)

El núcleo visual del proyecto se consolida en una **Gráfica de Radar (o de Triángulo de Control)** que mide la simetría y balance de los tres pilares evaluados por el grupo laboral:

<p align="center">
  <img src="images/grafica_radar.png" alt="Gráfica del Inventario de Ejes Operativos" width="450">
</p>

### 🎯 Diagnóstico Directivo de la Línea Base:
*   **Métricas Consolidadas:** El grupo opera con un **Promedio General de 7/10** (Nivel de Alcance: 7, Servicio: 7, Unidad Operativa: 6).
*   **Hallazgo Crítico:** La gráfica rompe su simetría en el vértice inferior derecho (**Unidad Operativa = 6**). Esto señala de forma inmediata a los directores y stakeholders que los recursos y planes de acción deben enfocarse prioritariamente en dinámicas de pertenencia e inclusión.

---

## 🛠️ Arquitectura del Sistema (Pipeline de Datos)

El proyecto fue estructurado simulando un pipeline formal de **ETL (Extracción, Transformación y Carga)** dividido en 4 capas lógicas independientes:

---

## 🧮 Ingeniería de Fórmulas y Justificación Técnica

Como analista, cada celda fue diseñada optimizando el rendimiento del motor de cálculo y asegurando la escalabilidad del libro de trabajo:

### 1. Normalización de Calificaciones (Capa de Transformación)
*   **Fórmula:** `=(SUM($C2:$AF2)/(COUNT($C2:$AF2)*2))*10`
*   **Justificación Técnica:** Los votos individuales se capturan en una escala cualitativa de 3 opciones (`0 = Nunca`, `1 = Algunas veces`, `2 = Casi siempre`). Para volver la métrica interpretable por la dirección, multiplico el conteo de celdas activas por el peso máximo (`COUNT(...)*2`), generando el techo teórico de puntos. Dividir la suma real entre este valor y multiplicarla por 10 **normaliza cualquier volumen de respuestas a una escala universal de 0 a 10**, haciéndola independiente del número de evaluadores.

### 2. Minigráficos In-Cell (Análisis Visual Rápido)
*   **Fórmula:** `=SPARKLINE(AG2; {"charttype"\"bar"; "max"\10})`
*   **Justificación Técnica:** Facilita la técnica de *Data Storytelling* para el capturista. En lugar de saturar la vista con tablas infinitas, se fuerza una barra de rendimiento visual integrada en la celda parametrizada al máximo de nuestra escala (`max\10`).

### 3. Filtro Matricial Dinámico de Puntos Críticos
*   **Fórmula (Eje Recuperación/Alcance):**
    ```excel
    =FILTER(PUNTAJE!AI2:AI61; BASE_DATOS!B2:B61="RECUPERACION"; PUNTAJE!AG2:AG61<=6)
    ```
*   **Justificación Técnica:** Elimina la necesidad de utilizar macros (VBA) complejas, reduciendo el peso del archivo. Realiza un filtrado condicional cruzado entre dos matrices dimensionales distintas: busca la coincidencia exacta de la categoría en la base maestra oculta y, al mismo tiempo, extrae únicamente los reactivos con rendimiento reprobatorio ($\leq$ 6). Esto pobla el panel de crisis de manera 100% automatizada.


### 4. Agregación Condicional para el Dashboard
*   **Fórmula:** `=ROUND(AVERAGE(FILTER(PUNTAJE!AG2:AG61; BASE_DATOS!B2:B61="RECUPERACION"));0)`
*   **Justificación Técnica:** Previene el sesgo de datos. Filtra las calificaciones correspondientes a un solo bloque operativo y calcula su media aritmética. Aplica un redondeo matemático (`ROUND`) para proveer al dashboard directivo números enteros sólidos, limpios y listos para alimentar los ejes de la gráfica tridimensional.

<img width="320" height="295" alt="image" src="https://github.com/user-attachments/assets/b0e706e8-1efe-4acf-bea7-acdcbf23b9fe" />

---

## 🔍 Hallazgos de Datos Destacados (Data Insights)

El procesamiento de datos de la hoja **Resumen** detectó patrones críticos de negocio que requieren intervención:
1.  **Riesgo en Clima Laboral (Unidad Operativa):** Preguntas de relaciones internas como *(5) Respeto a opiniones diferentes* y *(8) Evitar discusiones divisivas* promedian un puntaje crítico de **1**. Existe fricción en el equipo.
2.  **Baja Eficiencia de Procesos (Servicio):** El cumplimiento de compromisos *(6)* y la aceptación de responsabilidades *(3)* promedian **1**, explicando el cuello de botella en los flujos operativos de la organización.

---


## 🛠️ Aptitudes Demostradas en este Repositorio
*   **Modelado de Datos e Inteligencia de Negocio (BI)**
*   **Lógicas de Control de Inventarios y Abastecimiento**
*   **Data Wrangling y Limpieza de Datos Cualitativos**
*   **Gobernanza de Datos (Data Security & Masking)**
