# Reporte de Análisis Electromiográfico (EMG)

## 1. Resumen de Mediciones
| Sujeto | Músculo Evaluado | Archivo de Origen | Frecuencia de Muestreo | Amplitud Máxima Aprox. |
| :--- | :--- | :--- | :--- | :--- |
| **Leo** | Tríceps Braquial | `triceps leo.h5` | 1000 Hz | $\approx 1.5\text{ mV}$ |
| **Kevin** | Tríceps Braquial | `triceps kevin.h5` | 1000 Hz | $> 1.5\text{ mV}$ (Saturada) |
| **Kevin** | Bíceps Braquial | `biceps kevin.h5` | 1000 Hz | $> 1.5\text{ mV}$ (Saturada) |

---

## 2. Visualización de las Señales

### A. Tríceps - Leo (`triceps leo.h5`)
![EMG Tríceps Leo](tricep%20leo.png)
* **Observación:** Curva progresiva con incremento gradual en el reclutamiento de fibras musculares. Alcanza un pico máximo claro cercano a $1.5\text{ mV}$ sin recortes en la señal.

---

### B. Tríceps - Kevin (`triceps kevin.h5`)
![EMG Tríceps Kevin](tricep%20kevin.png)
* **Observación:** Señal con contracción de alta intensidad sostenida. Muestra saturación en los extremos superiores e inferiores al exceder el rango dinámico del sensor BITalino.

---

### C. Bíceps - Kevin (`biceps kevin.h5`)
![EMG Bíceps Kevin](bicep%20kevin.png)
* **Observación:** Fase inicial de activación moderada seguida de un pico de esfuerzo máximo sostenido con reclutamiento completo y saturación de la señal.

---

## 3. Discusión y Comparativa
* **Calidad de la Señal:** Las tres mediciones presentan una línea base muy limpia en reposo ($0\text{ mV}$), confirmando una adecuada colocación de los electrodos de referencia y bajo ruido de interferencia.
* **Saturación:** En las pruebas de Kevin se superó el límite de voltaje de entrada del canal analógico ($A1$), lo cual genera un "corte" superior e inferior. Para análisis estadísticos cuantitativos (como RMS o área bajo la curva), la señal de Leo es la más idónea por no presentar clipping.

---

## 4. Conclusión
Se registraron exitosamente los patrones de activación EMG para el bíceps y tríceps braquial. Las ráfagas reflejan fielmente el esfuerzo neuromuscular durante las contracciones isométricas e isotónicas analizadas.