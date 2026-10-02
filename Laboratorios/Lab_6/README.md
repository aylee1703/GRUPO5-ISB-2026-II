<div align="center">

# Laboratorio 6

<img width="600" height="200" alt="Universidad Peruana Cayetano Heredia" src="https://github.com/user-attachments/assets/294153a6-16c6-40be-b47a-d5d1e62aee72" />

### Adquisición y análisis de señales electroencefalográficas (EEG)

</div>

---

## Paso a paso para la adquisición de las señales EEG

### 1. Materiales

- Software OpenSignals (r)evolution
- BITalino Core BT
- Sensor EEG ensamblado (configuración bipolar, IN+ / IN−)
- Cable de referencia de 1 derivación
- Electrodos de gel Ag/AgCl (2 para el sensor y 1 para la referencia)
- Audífonos y dispositivo de música

### 2. Preparación del equipo

1. Abrir OpenSignals (r)evolution en la computadora.
2. Encender el BITalino Core BT.
3. Conectar el sensor EEG y el cable de referencia al BITalino.
4. Configurar el canal activo.

### 3. Colocación de los electrodos

1. Colocar los electrodos de gel en los dos broches del sensor EEG y uno en el cable de referencia.
2. Colocar los 2 electrodos del sensor en la frente.
3. Colocar el electrodo de referencia detrás de la oreja.

### 4. Protocolo de adquisición

| Etapa | Descripción |
|---|---|
| **Lectura basal** (≈ 1–2 min) | Sin estímulos externos. Se le taparon al sujeto los ojos y los oídos para que no percibiera nada. |
| **Ciclos de ojos abiertos / cerrados** | Se dio la señal de inicio con un toque en el hombro. Se realizaron 5 repeticiones del ciclo, con 5 s entre el cierre y la apertura de los ojos. |
| **Preguntas complejas** | Se hicieron 5 preguntas. Cada pregunta se grabó en una señal individual (1 pregunta = 1 señal), con 30 s para pensar la respuesta antes de pasar a la siguiente. |
| **Música suave** | Se grabó una señal individual mientras el sujeto escuchaba música suave. |
| **Música fuerte** | Se grabó una señal individual mientras el sujeto escuchaba una canción de música fuerte. |

> **Nota:** Todo el procedimiento se realizó 2 veces.

## 5. Resultados

<div align="center">
<img width="1490" height="989" alt="bas" src="https://github.com/user-attachments/assets/cddeebf3-7c70-47a9-a70e-b59f6eafcc31" />
  
</div>

*Figura 1. Señal EEG en lectura basal (ojos y oídos cubiertos, sin estímulos externos), antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la transformada rápida de Fourier (FFT) y la densidad espectral de potencia (PSD) estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="ab_cerrar" src="https://github.com/user-attachments/assets/90419218-b8cd-4c63-a29e-453ec34b01f8" />

</div>

*Figura 2. Señal EEG durante los ciclos de apertura y cierre de ojos, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="preg1" src="https://github.com/user-attachments/assets/4ef7b184-d669-4400-84be-e6f91e53106c" />

</div>

*Figura 3. Señal EEG durante la pregunta compleja 1, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="preg2" src="https://github.com/user-attachments/assets/5c84fe82-9fe9-4349-b80b-eecf8e9d6c6c" />

</div>

*Figura 4. Señal EEG durante la pregunta compleja 2, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="preg3" src="https://github.com/user-attachments/assets/cb4d66eb-634e-42f4-81dc-7e3843237c43" />

</div>

*Figura 5. Señal EEG durante la pregunta compleja 3 (30 s para pensar la respuesta), antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="preg4" src="https://github.com/user-attachments/assets/28697db9-cf8d-42fe-bf05-fcb5a9c3426a" />

</div>

*Figura 6. Señal EEG durante la pregunta compleja 4, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="preg5" src="https://github.com/user-attachments/assets/a11dce9e-85ce-4014-b1f5-97f365902782" />

</div>

*Figura 7. Señal EEG durante la pregunta compleja 5, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="musica_fuerte" src="https://github.com/user-attachments/assets/1e24a5cd-6dd8-4d52-a532-6a8decb7e305" />

</div>

*Figura 8. Señal EEG mientras el sujeto escuchaba música fuerte, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

<div align="center">
<img width="1490" height="989" alt="musica_suave" src="https://github.com/user-attachments/assets/0df1616f-7279-4c25-ad86-2d5f542f9c12" />

</div>

*Figura 9. Señal EEG mientras el sujeto escuchaba música suave, antes y después del filtrado pasabanda Butterworth de 4.° orden (1–40 Hz). Se muestran los primeros 20 s en el dominio del tiempo, la FFT y la PSD estimada con el método de Welch.*

## 6. Discusión

### Estimación espectral: FFT vs. método de Welch

Para cuantificar la potencia de los ritmos cerebrales se utilizó el método de Welch además de la FFT. La FFT de un segmento único de 20 s presenta una alta varianza: cada componente frecuencial se estima a partir de una sola realización de la señal, lo que produce el aspecto ruidoso y con picos aislados observado en todas las figuras. El método de Welch divide la señal en ventanas solapadas (en este caso, ventanas de 2 s con 50 % de solapamiento, es decir, unas 19 ventanas por registro), calcula el periodograma de cada una y los promedia. Esto reduce la varianza a costa de una menor resolución en frecuencia (0.5 Hz), lo cual es suficiente para analizar bandas de varios hertz de ancho como Delta, Theta, Alfa, Beta y Gamma [1].

### Efecto del filtrado (1–40 Hz)

En todos los registros, la señal original presentó una deriva de línea base de gran amplitud, visible como oscilaciones lentas en el dominio del tiempo y como un pico dominante cerca de 0 Hz en la FFT original. Esta deriva se asocia a variaciones en la impedancia piel-electrodo, sudoración y movimientos del sujeto, y no a actividad cerebral [2]. El filtro pasabanda eliminó esta componente de forma consistente: tras el filtrado, las señales quedaron centradas en cero y el espectro mostró con claridad la actividad entre 1 y 15 Hz, antes oculta por la deriva. Un ejemplo claro es la Figura 5, donde una deflexión lenta de gran amplitud cerca de los 11 s, probablemente un movimiento ocular o de cabeza, desaparece casi por completo en la señal filtrada.

Sin embargo, el filtrado tiene límites. En los registros donde la señal saturó el rango del conversor analógico-digital (Figuras 2 y 8), los tramos recortados no pueden recuperarse, porque la información se perdió en la adquisición. En la Figura 8, por ejemplo, la señal filtrada es prácticamente nula durante el primer segundo, lo que no corresponde a ausencia de actividad cerebral, sino a que el tramo saturado es constante.

### Interferencia de la red eléctrica y aliasing

En la mayoría de registros, la PSD original muestra un pico estrecho en 40 Hz, especialmente marcado en la Figura 7. Este pico no corresponde a actividad cerebral: la actividad neuronal ocupa bandas anchas, mientras que una línea espectral tan angosta es característica de una interferencia sinusoidal. Su origen más probable es la red eléctrica de 60 Hz, que al muestrearse a 100 Hz (por encima de la frecuencia de Nyquist de 50 Hz) se refleja en |60 − 100| = 40 Hz por aliasing [3]. Como esta frecuencia coincide con el corte superior del filtro, donde la atenuación es de solo unos 6 dB (por el doble paso de `filtfilt`), la interferencia no se elimina por completo. Para futuras adquisiciones, se recomienda muestrear a 1000 Hz y aplicar un filtro notch en 60 Hz.

### Lectura basal

En la lectura basal (Figura 1), con ojos y oídos cubiertos, la energía de la señal filtrada se concentró entre 1 y 8 Hz (Delta y Theta), sin un pico claro en la banda Alfa. Aunque el ritmo Alfa es el marcador clásico del reposo, este es más prominente en regiones occipitales y parietales [4]. Con electrodos ubicados en la frente, la contribución Alfa es menor y la señal está más expuesta a artefactos oculares, que concentran su energía en frecuencias bajas. Los picos de mayor amplitud en los primeros 8 s del registro son compatibles con movimientos oculares, que los electrodos frontales captan aun con los ojos cubiertos.

### Apertura y cierre de ojos

La Figura 2 es el único registro en el que aparece un pico definido en la banda Alfa, cerca de 11–12 Hz, visible tanto en la FFT como en la PSD filtradas. Este resultado es coherente con la reactividad Alfa: la potencia Alfa aumenta al cerrar los ojos y disminuye al abrirlos, fenómeno conocido como bloqueo Alfa [4]. Al mismo tiempo, es el registro con más artefactos: cada apertura y cierre de ojos generó un potencial ocular (EOG) de gran amplitud que saturó el amplificador entre los 5 y 14 s. Esto muestra la principal desventaja de la colocación frontal: maximiza la contaminación ocular justo en la tarea donde los ojos se mueven deliberadamente.

### Preguntas complejas

En las cinco preguntas (Figuras 3 a 7), la energía se concentró principalmente en Delta y Theta, sin pico Alfa, lo que es coherente con un estado de procesamiento cognitivo activo, en el cual el ritmo Alfa tiende a suprimirse [5]. En las preguntas 1, 4 y 5 se observó una actividad destacada en Theta (entre 4 y 7 Hz), con picos cerca de 6.3 Hz en la pregunta 4 y de 5–6 Hz en la pregunta 5. Este hallazgo es relevante porque el *Theta frontal de línea media* se asocia al esfuerzo mental, la memoria de trabajo y el cálculo, y se registra justamente en la región frontal [5], [6].

La respuesta no fue uniforme entre preguntas: la pregunta 2 mostró menor actividad Theta y la pregunta 3 fue el registro de menor amplitud, lo que podría reflejar diferencias en la dificultad percibida de cada pregunta. Además, en las preguntas 2, 3 y 4 la actividad aumentó en la segunda mitad del registro, posiblemente cuando el sujeto empezaba a formular su respuesta y aparecían movimientos faciales u oculares. Como no se marcaron eventos durante la adquisición, esta interpretación no puede confirmarse.

Cabe señalar que no se observó un aumento claro en la banda Beta, a pesar de que la teoría la asocia a la actividad cognitiva. Con una sola derivación frontal y segmentos de 20 s, la sensibilidad para detectar este cambio es limitada.

### Música fuerte vs. música suave

La comparación entre ambas condiciones musicales muestra el contraste más claro del laboratorio. Con música fuerte (Figura 8), la PSD original mantuvo un nivel más alto en frecuencias altas (cerca de −12 dB/Hz entre 35 y 45 Hz, frente a unos −20 dB/Hz en las demás condiciones) y aparecieron pequeños picos en Beta, cerca de 17, 23 y 30 Hz. Con música suave (Figura 9), la señal filtrada tuvo la menor amplitud de todo el laboratorio, la PSD alcanzó su máximo más bajo y el contenido en frecuencias altas volvió a niveles similares a los de la lectura basal.

El aumento en Beta y Gamma con música fuerte es compatible con un estado de mayor activación, pero también con contaminación por actividad muscular (EMG). Los músculos de la frente, la mandíbula y el cuero cabelludo generan señales de banda ancha que contaminan Beta y Gamma, sobre todo en derivaciones frontales [7]. Si el sujeto tensó el rostro o se movió al ritmo de la música, ambos efectos se superponen y no pueden separarse con una sola derivación. La gran deriva de línea base registrada en esta condición, la mayor de todas, apoya la posibilidad de que hubo movimiento.

### Limitaciones

- Se analizó un solo sujeto y solo los primeros 20 s de cada registro, por lo que los resultados no pueden generalizarse.
- La amplitud se expresó en unidades del conversor analógico-digital, sin conversión a µV, lo que impide comparar valores absolutos con la literatura.
- La frecuencia de muestreo de 100 Hz limitó el análisis de Gamma a 40 Hz y produjo aliasing de la red eléctrica.
- La ubicación frontal de los electrodos favorece la captación de artefactos oculares y musculares y reduce la detección del ritmo Alfa.
- Las comparaciones entre condiciones se basaron en la inspección visual de las gráficas. Calcular la potencia relativa por banda en cada condición permitiría respaldarlas cuantitativamente.

## Referencias

[1] P. Welch, "The use of fast Fourier transform for the estimation of power spectra: A method based on time averaging over short, modified periodograms," *IEEE Trans. Audio Electroacoust.*, vol. 15, no. 2, pp. 70–73, 1967.

[2] J. A. Urigüen y B. Garcia-Zapirain, "EEG artifact removal—state-of-the-art and guidelines," *J. Neural Eng.*, vol. 12, no. 3, Art. no. 031001, 2015.

[3] A. V. Oppenheim y R. W. Schafer, *Discrete-Time Signal Processing*, 3rd ed. Upper Saddle River, NJ, USA: Pearson, 2010.

[4] R. J. Barry, A. R. Clarke, S. J. Johnstone, C. A. Magee y J. A. Rushby, "EEG differences between eyes-closed and eyes-open resting conditions," *Clin. Neurophysiol.*, vol. 118, no. 12, pp. 2765–2773, 2007.

[5] W. Klimesch, "EEG alpha and theta oscillations reflect cognitive and memory performance: A review and analysis," *Brain Res. Rev.*, vol. 29, no. 2–3, pp. 169–195, 1999.

[6] D. J. Mitchell, N. McNaughton, D. Flanagan y I. J. Kirk, "Frontal-midline theta from the perspective of hippocampal 'theta'," *Prog. Neurobiol.*, vol. 86, no. 3, pp. 156–185, 2008.

[7] I. I. Goncharova, D. J. McFarland, T. M. Vaughan y J. R. Wolpaw, "EMG contamination of EEG: Spectral and topographical characteristics," *Clin. Neurophysiol.*, vol. 114, no. 9, pp. 1580–1593, 2003.
