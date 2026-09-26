# Laboratorio 5: Sistema de monitoreo de estrés y fatiga mental mediante ECG

## Descripción

Este proyecto propone el desarrollo de un sistema para el monitoreo de indicadores fisiológicos asociados con el **estrés y la fatiga mental** mediante el procesamiento de señales electrocardiográficas (ECG).

La propuesta utiliza la información temporal del ECG para identificar los picos R, calcular los intervalos RR y obtener parámetros de **variabilidad de la frecuencia cardíaca (HRV)**. A partir de estas características se busca diferenciar estados fisiológicos asociados con condiciones de reposo, estrés y recuperación.

El sistema se plantea como una herramienta de monitoreo y análisis de señales biomédicas, no como un método de diagnóstico clínico.

---

## 1. Planteamiento del problema

El estrés puede producir modificaciones en la actividad del sistema nervioso autónomo y, en consecuencia, generar cambios en la dinámica cardiovascular. Sin embargo, su evaluación suele depender de cuestionarios, autorreportes o mediciones realizadas durante periodos limitados.

Estas estrategias presentan tres limitaciones principales:

- **Subjetividad:** dependen de la percepción y respuesta del individuo.
- **Evaluación reactiva:** el problema puede identificarse después de la aparición de síntomas.
- **Medición discontinua:** las evaluaciones aisladas no permiten observar variaciones fisiológicas durante diferentes actividades.

Por ello, resulta relevante explorar métodos cuantitativos basados en señales fisiológicas que permitan caracterizar cambios asociados con la respuesta al estrés.

---

## 2. Fundamento fisiológico

La respuesta al estrés está relacionada con cambios en la regulación del **sistema nervioso autónomo (SNA)**. La activación simpática y parasimpática modifica la dinámica del ritmo cardíaco y, por tanto, los intervalos de tiempo entre latidos consecutivos.

En una señal ECG, estos cambios pueden estudiarse mediante los **intervalos RR**, definidos como el tiempo entre dos picos R consecutivos.

La variación de estos intervalos permite calcular la **variabilidad de la frecuencia cardíaca (HRV)**, utilizada como indicador de la modulación autonómica cardíaca.

De manera general:

- Una mayor activación simpática puede asociarse con una reducción de determinados índices de HRV.
- Una mayor actividad parasimpática puede asociarse con una mayor variabilidad entre latidos.

Por esta razón, el análisis de HRV constituye la base fisiológica empleada en este proyecto para estudiar cambios asociados con estrés y recuperación.

---

## 3. Objetivo

Desarrollar un sistema de procesamiento de señales ECG capaz de extraer características de variabilidad cardíaca y utilizarlas para identificar cambios fisiológicos asociados con diferentes estados de estrés.

### Objetivos específicos

1. Adquirir señales ECG mediante un sistema de instrumentación biomédica o utilizar registros de una base de datos.
2. Preprocesar la señal para reducir interferencias y componentes no deseados.
3. Detectar los picos R y calcular los intervalos RR.
4. Extraer parámetros de HRV relevantes para el análisis.
5. Clasificar o representar los estados fisiológicos analizados mediante una interfaz de visualización.

---

## 4. Propuesta del sistema

El sistema se estructura como una cadena de procesamiento de señales biomédicas:

**ECG → Preprocesamiento → Detección de picos R → Intervalos RR → HRV → Clasificación → Visualización**

La metodología se divide en cuatro etapas principales.

### Etapa 1. Adquisición

La señal ECG puede obtenerse mediante:

- Sistema de adquisición **BITalino**, para registros experimentales.
- Base de datos **WESAD**, para trabajar con registros previamente adquiridos y etiquetados.

La señal ECG constituye la entrada principal del sistema.

### Etapa 2. Preprocesamiento

La señal adquirida se acondiciona antes de realizar la extracción de características.

Se plantea aplicar:

- **Filtro notch de 60 Hz**, para reducir la interferencia asociada a la red eléctrica.
- **Filtro pasa-banda de 0.5–45 Hz**, para conservar las principales componentes de interés del ECG y reducir componentes fuera de banda.

El resultado de esta etapa es una señal acondicionada para la detección de los complejos QRS.

### Etapa 3. Extracción de características

A partir de la señal ECG preprocesada se identifican los **picos R**.

Posteriormente, se calculan los intervalos RR:

\[
RR_i = t_{R_{i+1}} - t_{R_i}
\]

donde \(t_{R_i}\) representa el instante temporal correspondiente al pico R.

La secuencia de intervalos RR permite construir el **tacograma** y calcular parámetros de HRV. Entre los indicadores considerados se encuentran:

- **SDNN:** desviación estándar de los intervalos NN.
- **RMSSD:** raíz cuadrática de la media de las diferencias sucesivas entre intervalos NN.

Estos parámetros permiten cuantificar diferentes componentes de la variabilidad cardíaca.

### Etapa 4. Clasificación y visualización

Las características obtenidas de la señal se utilizan para analizar diferencias entre estados fisiológicos.

Se consideran tres condiciones:

- **Neutral o reposo**
- **Estrés**
- **Recuperación**

Finalmente, los resultados pueden mostrarse mediante un **dashboard**, permitiendo visualizar la señal ECG, los intervalos RR, los parámetros de HRV y el estado identificado.

---

## 5. Flujo de procesamiento

```text
        Señal ECG
            │
            ▼
     Adquisición de datos
            │
            ▼
      Preprocesamiento
     ┌─────────────────┐
     │ Notch de 60 Hz  │
     │ BP 0.5–45 Hz    │
     └─────────────────┘
            │
            ▼
    Detección de picos R
            │
            ▼
      Intervalos RR
            │
            ▼
         Tacograma
            │
            ▼
     Extracción de HRV
       SDNN / RMSSD
            │
            ▼
        Clasificación
            │
            ▼
 Neutral / Estrés / Recuperación
            │
            ▼
        Visualización
```

---

## 6. Resultado esperado

Se espera implementar una cadena de procesamiento capaz de transformar una señal ECG cruda en parámetros cuantitativos de HRV.

El sistema deberá permitir:

1. Visualizar la señal ECG adquirida.
2. Reducir interferencias presentes en el registro.
3. Identificar los picos R.
4. Generar la serie de intervalos RR.
5. Calcular indicadores como SDNN y RMSSD.
6. Representar las características obtenidas para analizar diferencias entre estados de reposo, estrés y recuperación.

El proyecto busca demostrar la aplicación del **procesamiento digital de señales biomédicas** para obtener información fisiológica relevante a partir del ECG.

---

## 7. Alcance

El proyecto se desarrolla con fines académicos y experimentales. Los indicadores obtenidos mediante ECG y HRV permiten estudiar cambios en la regulación autonómica asociados con el estrés, pero **no constituyen por sí solos un diagnóstico médico o psicológico**.

La propuesta se centra en la adquisición, procesamiento, extracción de características y análisis de la señal ECG.

---

## 8. Tecnologías y recursos

| Componente | Aplicación |
|---|---|
| ECG | Señal fisiológica de entrada |
| BITalino | Adquisición experimental de ECG |
| WESAD | Base de datos para evaluación con registros existentes |
| Filtro notch | Atenuación de interferencia de 60 Hz |
| Filtro pasa-banda | Acondicionamiento de la señal ECG |
| Detección de picos R | Identificación de cada ciclo cardíaco |
| Intervalos RR | Construcción de la serie temporal cardíaca |
| HRV | Extracción de características |
| SDNN / RMSSD | Indicadores temporales de HRV |
| Dashboard | Visualización de resultados |

---

## 9. Referencias

[1] World Health Organization and International Labour Organization, *Mental health at work: Policy brief*. Geneva, Switzerland, 2022.

[2] S. Cohen, T. Kamarck, and R. Mermelstein, “A global measure of perceived stress,” *Journal of Health and Social Behavior*, vol. 24, no. 4, pp. 385–396, 1983.

[3] H.-G. Kim, E.-J. Cheon, D.-S. Bai, Y. H. Lee, and B.-H. Koo, “Stress and heart rate variability: A meta-analysis,” *Psychiatry Investigation*, vol. 15, no. 3, pp. 235–245, 2018. DOI: 10.30773/pi.2017.08.17.

[4] Task Force of the European Society of Cardiology and the North American Society of Pacing and Electrophysiology, “Heart rate variability: Standards of measurement, physiological interpretation, and clinical use,” *Circulation*, vol. 93, no. 5, pp. 1043–1065, 1996.