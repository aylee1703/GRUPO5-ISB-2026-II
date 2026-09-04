

## Respuestas a los Ejercicios y Preguntas de Análisis

### Pregunta Inicial
**¿Qué cree que representa `CHANNEL = 0`?**  
Representa el canal de señal del ECG (electrocardiograma) que fue grabado en la adquisición.

---

### Preguntas de Análisis 1 (Información del Registro)

1. **¿Cuál es la frecuencia de muestreo del registro?**  
   $$f_s = 360\text{ Hz}$$

2. **¿Cuántos canales tiene?**  
   Tiene **2 canales** (`MLII` y `V5`).

3. **¿Cómo se llama el canal seleccionado?**  
   `MLII` (el cual corresponde al canal `0`).

4. **¿Cuál es la duración total del registro?**  
   **1805.56 segundos** (aproximadamente 30.09 minutos).

5. **Si $f_s = 360\text{ Hz}$, ¿cuántas muestras se adquieren en 1 segundo?**  
   Se adquieren **360 muestras**.

6. **¿Cuántas muestras corresponden a un segmento de 10 segundos?**  
   **3600 muestras** ($360 \times 10$).

---

### Preguntas de Análisis 2 (Visualización del Registro Completo)

1. **¿La señal presenta una amplitud constante?**  
   No, la amplitud va cambiando constantemente por el latido del corazón.

2. **¿Se pueden identificar visualmente complejos QRS?**  
   No se pueden visualizar muy claro ya que la señal muestra 30 minutos enteros juntos, por lo que no es posible distinguir cada latido por separado.

3. **¿La morfología permanece igual durante todo el registro?**  
   A primera vista, parece que permanece igual; sin embargo, hay zonas donde la señal se mueve hacia arriba o hacia abajo y presenta picos extraños.

4. **¿Se observa ruido?**  
   Sí, hay ruido en la línea base (donde la señal sube y baja); asimismo, alrededor del segundo 1520 se observa un pico gigante hacia abajo.

5. **¿Qué ventajas tiene visualizar una señal durante varios minutos?**  
   Nos ayuda a ver el estado general del paciente para saber si el corazón estuvo tranquilo durante toda la prueba o si en algún momento tuvo un susto, fallo o alteración que no saldría si solo tuviéramos una señal de 5 segundos.

6. **¿Qué limitaciones tiene una gráfica demasiado extensa?**  
   Que todo se ve apretado: al meter toda la información en una sola imagen, se pierden los detalles minuciosos y ya no se pueden distinguir la forma de las ondas (como la P, el complejo QRS o la T).

---

### Preguntas de Análisis 3 (Histograma y Distribución de Amplitud)

1. **¿Dónde se concentra la mayor cantidad de muestras?**  
   La mayor cantidad de muestras se encuentra entre **-0.4 mV y -0.2 mV**. Esto ocurre ya que casi todo el tiempo el corazón se encuentra en "reposo" (línea isoeléctrica).

2. **¿La distribución parece simétrica?**  
   No, ya que tiene valores que se encuentran desplazados hacia la derecha la mayor parte del tiempo, permaneciendo en valores bajos.

3. **¿Existen valores extremos?**  
   Sí, existen valores extremos que llegan cerca de **1.0 mV** en la parte positiva y cerca de **-0.6 mV** en la parte negativa.

4. **¿Qué podría producir valores de amplitud muy diferentes al valor central?**  
   Los picos R cuando el corazón se contrae, así como el ruido producido cuando el paciente se mueve o si el electrodo roza con alguna superficie.

5. **¿El histograma conserva información temporal? Explique.**  
   **No**, el histograma solo cuenta cuántas veces se repitió una determinada amplitud dentro de la señal, pero mezcla todas las muestras perdiendo la secuencia y el orden temporal en que ocurrieron.

---

### Preguntas de Análisis 4 (Muestreo y Eje Temporal Discreto)

1. **¿Cuántas muestras existen por segundo?**  
   Aproximadamente **360 muestras**.

2. **¿Qué ocurre si aumentamos $f_s$?**  
   Tomamos más muestras por segundo. La ventaja es que se pueden mostrar más puntos en la señal (mayor resolución temporal), pero la desventaja es que el archivo se vuelve más pesado.

3. **¿Qué ocurre si disminuimos $f_s$?**  
   Tomamos menos muestras por segundo, guardamos menos datos y la señal se empieza a ver sin forma, pudiendo perderse detalles importantes.

4. **¿Qué representa el eje $n$ en una señal discreta?**  
   Es la posición o el número de muestra ($n = 0, 1, 2, \dots$).

5. **¿Cuál es la relación entre $n$, $f_s$ y $t$?**  
   Existe la relación:
   $$t = \frac{n}{f_s}$$
   Esta fórmula nos sirve para saber en qué segundo exacto ocurrió determinada muestra.

---

### Preguntas de Análisis 5 (Conversión a Audio WAV)
> **Nota:** No se pudo escuchar el audio, por lo que no fue posible responder a las preguntas 1 a 6 de esta sección.

---

### Ejercicio 1: Comparación entre Registro 100 y Registro 200

* **Frecuencia de muestreo:** Ambas señales tienen la misma frecuencia ($360\text{ Hz}$) ya que comparten la misma tasa de muestreo de la base de datos.
* **Número de canales:** Los dos registros cuentan con **2 canales** de grabación en paralelo.
* **Nombres de canales:** Mantienen los mismos nombres (`MLII` y `V1`).
* **Morfología:** El registro `100` muestra un ritmo sinusal uniforme, mientras que el registro `200` presenta una morfología irregular con presencia de extrasístoles ventriculares (latidos anómalos anchos y picos invertidos).
* **Amplitud:** El registro `100` oscila mayormente entre **-0.5 mV y 1.2 mV**. El registro `200` expande su rango bruscamente, pues alcanza picos negativos hasta **-2.2 mV** y positivos superiores a **1.1 mV**.
* **Distribución:** El histograma del registro `200` es mucho más asimétrico y disperso, mostrando una cola prominente en los valores negativos generada por la caída de voltaje de los latidos atípicos. En resumen, el registro `100` presenta un ECG normal que se observa de manera estable y uniforme, mientras que el registro `200` muestra una patología clara (extrasístoles ventriculares) que distorsiona la forma de la onda, duplica el rango de voltaje llegando hasta **-2.2 mV** y ensancha la distribución en el histograma.

### Ejercicio 2: Análisis del Segundo Canal (`V5`)

1. **¿Qué nombre tiene el nuevo canal?**  
   `V5`

2. **¿Tiene las mismas unidades?**  
   Sí, se mantiene en **mV** (milivoltios).

3. **¿La morfología es igual?**  
   No, la morfología cambia significativamente respecto al canal 0 (`MLII`).

4. **¿Qué diferencias observa?**  
   Cambia la orientación y la amplitud del complejo QRS.

---

### Ejercicio 3: Comparación de Ventanas de Visualización

* **Explique por qué una duración demasiado pequeña o demasiado grande puede dificultar el análisis:**  
  La comparación entre ambas demuestra que una duración de **5 s** permite inspeccionar a detalle la morfología de las ondas e identificar el ruido; sin embargo, abarca muy pocos latidos para evaluar el ritmo cardíaco. Por otro lado, una duración de **20 s** ayuda a visualizar la regularidad del ritmo cardíaco, pero comprime los ciclos cardíacos, lo que impide medir con precisión la duración de los intervalos y la amplitud de los picos.

---

### Ejercicio 4: Cálculos y Muestreo ($f_s = 360\text{ Hz}$)

#### a) Calcule el periodo de muestreo ($T_s$):
$$T_s = \frac{1}{f_s} = \frac{1}{360\text{ Hz}} \approx 0.00278\text{ s} = 2.78\text{ ms}$$

#### b) ¿Cuántas muestras existen en 5 segundos?
$$N_{5\text{s}} = f_s \times t = 360 \times 5 = 1800\text{ muestras}$$

#### c) ¿Cuántas muestras existen en 10 segundos?
$$N_{10\text{s}} = f_s \times t = 360 \times 10 = 3600\text{ muestras}$$

#### d) Explique qué sucedería si la frecuencia de muestreo fuese reducida significativamente:
En caso de que la frecuencia baje mucho, el sistema tomaría muy pocos puntos por segundo y la señal perdería definición. Seguidamente, los picos del ECG (como el complejo QRS) se verían deformados e incluso se podría incumplir el criterio de Nyquist, distorsionando la forma de la onda y conduciendo a un mal diagnóstico.

---
### Ejercicio 5: Análisis de Amplitud

A partir del segmento seleccionado, se obtuvieron los siguientes datos estadísticos:

1. **Media:** $0.0629 \text{ mV}$
2. **Desviación Estándar:** $0.2250 \text{ mV}$
3. **Valor Máximo:** $1.4350 \text{ mV}$
4. **Valor Mínimo:** $-0.6750 \text{ mV}$
5. **Rango:** $2.1100 \text{ mV}$

#### Interpretación de Parámetros

* **Media ($0.0629 \text{ mV}$):** Muestra que la señal está centrada en cero (sin nivel de DC u *offset*).
* **Desviación Estándar ($0.2250 \text{ mV}$):** Mide la dispersión del voltaje; refleja la variabilidad generada por los latidos.
* **Máximo ($1.4350 \text{ mV}$):** Deflexión positiva más alta, correspondiente a la **onda R**.
* **Mínimo ($-0.6750 \text{ mV}$):** Deflexión negativa más profunda, asociada a las **ondas Q o S**.
* **Rango ($2.1100 \text{ mV}$):** Voltaje pico a pico ($\text{Máx} - \text{Mín}$); establece el rango dinámico total.
---
## 3. Preguntas Conceptuales

1. **¿Qué es PhysioNet?**  
   Es un repositorio que cuenta con datos de señales biomédicas para estudio e investigación.

2. **¿Qué diferencia existe entre `DATABASE` y `RECORD`?**  
   `DATABASE` es la base de datos completa y `RECORD` es el archivo o registro de una persona en específico.

3. **¿Qué representa `fs`?**  
   La frecuencia de muestreo; indica cuántas muestras se toman por segundo.

4. **¿Qué representa `CHANNEL`?**  
   El canal del ECG que se va a graficar o analizar.

5. **¿Qué representa `record.p_signal`?**  
   La matriz que contiene los valores de voltaje de la señal expresados en mV.

6. **¿Por qué necesitamos construir un eje temporal?**  
   Porque los datos en origen vienen etiquetados por número de muestra ($n$) y necesitamos convertirlos a segundos reales ($t$) para su correcta interpretación clínica.

7. **¿Qué diferencia existe entre una señal continua y una señal discreta?**  
   La señal continua existe en todo instante de tiempo, mientras que la discreta solo toma valores en puntos temporales específicos.

8. **¿Por qué no debemos interpretar directamente un archivo WAV como si fuera una señal ECG?**  
   Porque el formato WAV está diseñado para audio y procesamiento acústico, no para calibraciones cuantitativas de voltaje biomédico.

9. **¿Qué ventajas ofrece trabajar con señales biomédicas reales en lugar de señales sintéticas?**  
   Nos permite analizar variaciones reales del paciente, ruidos biológicos auténticos y patologías complejas.

10. **¿Qué dificultades encontró durante el laboratorio?**  
    Había partes de los códigos un poco difíciles de entender y, en mi caso, no pude escuchar el audio para responder las preguntas requeridas en esa sección.
