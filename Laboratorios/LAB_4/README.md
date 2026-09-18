<div align="center">

# Laboratorio 5

<img width="850" height="300" alt="Universidad Peruana Cayetano Heredia" src="https://github.com/user-attachments/assets/294153a6-16c6-40be-b47a-d5d1e62aee72" />

### Adquisición y análisis de señales electrocardiográficas (ECG) en tres derivaciones mediante electrodos superficiales y el sistema BITalino

**Evaluación de la actividad cardíaca en reposo, hiperventilación, hipoventilación y actividad aeróbica**

</div>

---

## Introducción

La electrocardiografía (ECG) permite registrar de forma no invasiva la actividad eléctrica del corazón mediante electrodos colocados sobre la superficie corporal. En el trazado se identifican principalmente la onda P, el complejo QRS y la onda T, asociados con la despolarización auricular, la despolarización ventricular y la repolarización ventricular, respectivamente [1], [2].

En esta práctica se empleó el sistema **BITalino** con su sensor ECG y el software **OpenSignals** para adquirir las derivaciones bipolares I, II y III de Einthoven, que permiten observar la actividad eléctrica cardíaca desde distintas orientaciones del plano frontal [2], [3]. Los registros se realizaron en cuatro condiciones: reposo basal, hiperventilación, hipoventilación y actividad aeróbica. El análisis se orientó a comparar la frecuencia cardíaca, la detección de picos R y la morfología del latido promedio entre las diferentes condiciones fisiológicas.

**Objetivo:** adquirir y analizar señales ECG en tres derivaciones para identificar cambios en la frecuencia cardíaca y en la morfología de la señal ante distintas condiciones fisiológicas.

## Metodología

### 1. Materiales y equipos

- Sistema de adquisición **BITalino**.
- Sensor de electrocardiografía (ECG) y tres electrodos superficiales desechables.
- Computadora portátil con **OpenSignals** para la adquisición de datos.
- Entorno de procesamiento utilizado para visualizar la señal, detectar picos R y calcular la frecuencia cardíaca.
- Cronómetro para controlar las maniobras respiratorias y la actividad física.

### 2. Configuración de electrodos y conexión

Se utilizaron tres electrodos superficiales para obtener las derivaciones I, II y III de Einthoven. La colocación anatómica, la polaridad de los terminales y la conexión del sensor ECG se verificaron de acuerdo con la guía oficial de BITalino [3]. Antes de cada registro se comprobó el contacto de los electrodos y la correcta recepción de la señal en OpenSignals.

<p align="center">
  <img src="https://github.com/user-attachments/assets/415bc0d4-8607-414c-97c0-1f3c39a65222" height="390"/>
</p>

<p align="center">
  <b>Figura M1:</b> Configuración de electrodos para la adquisición de las derivaciones ECG [3].
</p>

<p align="center">
  <img width="1600" height="738" alt="WhatsApp Image 2026-09-17 at 11 17 43 PM" src="https://github.com/user-attachments/assets/8a97b818-e271-408c-ab3a-12c44acdc5a5" />
</p>

<p align="center">
  <b>Figura M2:</b> Conexión del sistema BITalino durante la adquisición de la señal ECG. [Elaboración propia]
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/b6a2ee38-f45d-453f-a4be-39d1c502a91e" height="390"/>
</p>

<p align="center">
  <b>Figura M3:</b> Configuración de polaridad de los electrodos [3].
</p>

> Las figuras metodológicas se identifican como **M1–M3** para no alterar la numeración original de las figuras de resultados.

### Evidencia de la actividad física realizada

Como parte del protocolo experimental, el participante realizó actividad física aeróbica antes de la adquisición de las señales ECG. El siguiente video documenta la ejecución de la actividad utilizada para generar el estado fisiológico posterior al ejercicio.

https://github.com/user-attachments/assets/7ea11b55-9e37-4386-8d88-f96370765d86

**Video 1.** Evidencia de la actividad física realizada durante el protocolo experimental. [Elaboración propia]

### 3. Protocolo experimental

| Condición | Procedimiento | Registro |
|---|---|---|
| **Reposo basal** | El participante permaneció en reposo, evitando movimientos durante la adquisición. | Derivaciones I, II y III. |
| **Hiperventilación** | Se realizó una maniobra de respiración profunda y acelerada; inmediatamente después se adquirió la señal ECG. | Derivaciones I, II y III. |
| **Hipoventilación** | Se realizó una maniobra voluntaria de reducción/retención de la respiración y luego se registró la señal ECG. | Derivaciones I, II y III. |
| **Actividad aeróbica** | Se realizaron ejercicios aeróbicos antes de cada adquisición: polichinelas, trote y escaladores. | DI después de polichinelas, DII después de trotar y DIII después de escaladores. |

Las mediciones se realizaron procurando iniciar el registro inmediatamente después de cada maniobra para conservar el efecto fisiológico de la condición evaluada. La influencia de la respiración y del ejercicio sobre la frecuencia cardíaca y la señal ECG está documentada en la literatura fisiológica y experimental [4]–[8].

### 4. Procesamiento de la señal

Para cada registro se realizó el mismo flujo de análisis: **visualización de la señal ECG → limpieza de la señal → detección de picos R → cálculo de frecuencia cardíaca → segmentación de latidos → obtención del latido promedio**. A partir de estos resultados se compararon la frecuencia cardíaca, la amplitud de los picos R, la estabilidad del registro y la morfología de las ondas P, QRS y T entre las diferentes condiciones.

---

## Resultados

### I. Lectura basal en reposo

<img width="1269" height="879" alt="BAS_D1" src="https://github.com/user-attachments/assets/812ea086-9018-421d-9615-6a849e7d5a2d" />

**Figura 1:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG obtenida en reposo (I Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 59.0 bpm, con un pico de aproximadamente 61.5 bpm a los 7.5 segundos y una caída mínima de 57.5 bpm entre los 17 y 19 s, manteniéndose relativamente estable el resto del registro. Los picos R presentan amplitudes entre 0.13 y 0.2, y aunque la señal cruda muestra cierto nivel de ruido en la línea base, el promedio de latidos permite identificar con claridad la morfología de las ondas P, Q, R, S y T, sin alteraciones evidentes en la conducción.

<img width="1246" height="858" alt="BAS_D2" src="https://github.com/user-attachments/assets/2ff099cd-1662-45c4-aa1d-8e44dd363b4b" />

**Figura 2:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG obtenida en reposo (II Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 53.4 bpm, con picos de hasta 56.3 bpm a los 2 segundos y una caída mínima de aproximadamente 51 bpm entre los 16 y 17 s, evidenciando mayor variabilidad que en la I Derivada. Los picos R presentan amplitudes considerablemente mayores, entre 0.75 y 0.9, consistente con lo esperado en la II Derivada al ser el eje de mayor proyección eléctrica del corazón. El promedio de latidos muestra ondas P, Q, R, S y T bien definidas, con un ligero artefacto hacia el final del registro (~19-20 s) donde la señal cruda se aparta de la señal limpia.

<img width="1316" height="908" alt="BAS_D3" src="https://github.com/user-attachments/assets/40673202-592b-4bd5-8bf3-3190fef40e3e" />

**Figura 3:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG obtenida en reposo (III Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 60.8 bpm, con un valle de aproximadamente 56 bpm a los 3 segundos y un pico máximo de 65.6 bpm cerca de los 15 s, mostrando la mayor variabilidad de las tres derivaciones basales analizadas. Los picos R presentan amplitudes entre 0.6 y 0.75, y el promedio de latidos muestra una onda T claramente identificable pero con ondas P poco pronunciadas, sin evidencia de alteraciones en la conducción intraventricular.

### II. Señal ECG obtenida después de la hiperventilación

<img width="1316" height="902" alt="HIPER_D1" src="https://github.com/user-attachments/assets/964048be-6caa-4ab4-bb0e-c7f2d457cc10" />

**Figura 4:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG después de la hiperventilación (I Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 76.9 bpm, notablemente mayor que en la lectura basal (59.0 bpm), consistente con la respuesta simpática esperada ante la hiperventilación. La frecuencia oscila con mayor amplitud, alcanzando un pico de 86 bpm a los 16 s y un valle de aproximadamente 67.5 bpm cerca de los 6.5 s, reflejando una variabilidad cardíaca marcada asociada al patrón respiratorio acelerado. Hacia el final del registro (~19 s) se observa un artefacto puntual de gran amplitud negativa (cercano a -0.45), probablemente asociado a movimiento o ruido durante la maniobra. El promedio de latidos mantiene ondas P, Q, R, S y T identificables, aunque con mayor dispersión entre latidos individuales respecto a la condición basal, reflejando menor estabilidad morfológica bajo esta condición.

<img width="1316" height="899" alt="HIPER_D2" src="https://github.com/user-attachments/assets/364003c0-a8ed-4de8-8a7d-fe27d111c052" />

**Figura 5:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG después de la hiperventilación (II Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 77.7 bpm, cercana a la registrada en DI de hiperventilación (76.9 bpm), confirmando la elevación sostenida del ritmo respecto a la condición basal (53.4 bpm en DII). La frecuencia presenta una tendencia oscilatoria creciente hacia el final del registro, alcanzando un pico de 86 bpm cerca de los 17.5 s y un valle mínimo de 67.5 bpm a los 3 s. Los picos R muestran amplitudes altas y consistentes, entre 0.6 y 0.95, propias de la II Derivada. El promedio de latidos evidencia ondas P, Q, R, S y T bien definidas y con buena consistencia entre latidos individuales, sin alteraciones de conducción aparentes.

<img width="1316" height="903" alt="HIPO_D1" src="https://github.com/user-attachments/assets/befe690b-6fe8-457d-8eee-eb854376643e" />
<img width="1316" height="908" alt="HIPER_D3" src="https://github.com/user-attachments/assets/29d1b278-cf78-42db-a1e9-1dde1be641ae" />

**Figura 6:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG después de la hiperventilación (III Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 81.0 bpm, la más elevada entre las tres derivaciones bajo hiperventilación (76.9 bpm en DI, 77.7 bpm en DII), con una tendencia claramente ascendente a lo largo del registro: un valle inicial de 69 bpm a los 2 s seguido de un incremento progresivo hasta un pico de 90 bpm cerca de los 16.5 s. Esta tendencia creciente sostenida es consistente con una intensificación del efecto de la hiperventilación conforme avanza la maniobra. Los picos R muestran amplitudes entre 0.5 y 0.8, y el promedio de latidos presenta ondas P, Q, R, S y T bien definidas, con dispersión moderada entre latidos individuales hacia la fase de repolarización (onda T).

### III. Señal ECG obtenida después de la hipoventilación

<img width="1316" height="903" alt="HIPO_D1" src="https://github.com/user-attachments/assets/bf5025f8-1547-464b-801c-073e3ec7e2f9" />

**Figura 7:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG después de la hipoventilación (I Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 62.3 bpm, valor intermedio entre la lectura basal (59.0 bpm) y la hiperventilación (76.9 bpm) para esta derivación, con oscilaciones moderadas: un pico de 64.1 bpm a los 3.5 s y un valle marcado de 60.5 bpm cerca de los 10.5 s. Los picos R presentan amplitudes bajas, entre 0.09 y 0.15, notoriamente menores que en las condiciones anteriores, lo cual podría reflejar mayor ruido relativo en la señal cruda respecto a la amplitud de la señal cardíaca. El promedio de latidos muestra ondas P, Q, R, S y T identificables, aunque con mayor dispersión entre latidos individuales, consistente con la menor calidad de señal observada en el panel de "ECG signal and peaks".

<img width="1316" height="905" alt="HIPO_D2" src="https://github.com/user-attachments/assets/06ab3328-e1e6-438b-9a41-e7a99303a62c" />

**Figura 8:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG después de la hipoventilación (II Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 65.7 bpm, con un pico de 68.2 bpm entre los 3.5 y 4 s y una posterior disminución progresiva hasta un mínimo de 64.7 bpm cerca de los 13.5 s. Cabe notar que este registro fue analizado sobre un intervalo más corto (~14.5 s en lugar de 20 s), y presenta un artefacto significativo hacia el final (~13-14.5 s), donde la señal cruda se dispara a amplitudes de hasta 2.2, muy por encima del rango normal de los picos R previos (~0.65-0.7), y donde la calidad de señal ("Signal quality") cae notoriamente - probablemente asociado a movimiento o pérdida de contacto del electrodo. Fuera de este artefacto, los picos R muestran amplitudes consistentes entre 0.6 y 0.7, y el promedio de latidos evidencia ondas P, R y T bien definidas.

<img width="1316" height="909" alt="HIPO_D3" src="https://github.com/user-attachments/assets/879636ca-79e6-4dc0-ad01-ac5a045d312a" />

**Figura 9:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - ECG después de la hipoventilación (III Derivada). [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 63.1 bpm, con un pico de 66.4 bpm a los 2 s seguido de una disminución progresiva hasta un mínimo de 60.8 bpm cerca de los 18.5 s, tendencia descendente que sugiere una progresiva reducción de la frecuencia cardíaca conforme avanza la maniobra de hipoventilación. Esta es la señal más limpia y estable de las tres derivaciones bajo esta condición: los picos R muestran amplitudes muy consistentes, en torno a 0.6, con mínima variación entre latidos, y el promedio de latidos evidencia ondas P, R y T claramente definidas con muy baja dispersión entre latidos individuales, sin artefactos evidentes.

### IV. Señal ECG obtenida después de la actividad aeróbica

<img width="1316" height="900" alt="AERO_D1" src="https://github.com/user-attachments/assets/ba46399b-c7c3-4ba1-abe8-86ddd4f020f6" />

**Figura 10:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - Actividad aeróbica (I Derivada) polichinelas. [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 100.6 bpm, la más elevada registrada hasta ahora en esta derivación, con un incremento marcado hacia el final del registro donde alcanza un pico de 113 bpm cerca de los 15.5 s, seguido de una caída abrupta a 83 bpm a los 17.5 s, coherente con el esfuerzo físico y la posterior fase de recuperación. Los picos R presentan amplitudes entre 0.15 y 0.22, y el promedio de latidos muestra ondas P, Q, R, S y T identificables, aunque con notable dispersión entre latidos individuales, reflejando la inestabilidad propia del ritmo cardíaco durante y después del ejercicio.

<img width="1325" height="896" alt="AERO_D2" src="https://github.com/user-attachments/assets/7111b0cd-2d81-4692-94cb-7dfc8fcd5d7c" />

**Figura 11:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - Actividad aeróbica (II Derivada) trotar. [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 104.8 bpm, con un pico de 112.5 bpm cerca de los 6.5 s y una caída notoria hasta 94 bpm entre los 14 y 15 s. Los picos R muestran amplitudes altas y consistentes, entre 0.6 y 0.85, propias de la II Derivada. El promedio de latidos evidencia ondas P, Q, R, S y T bien definidas, con dispersión moderada entre latidos individuales, menor que en la I Derivada, lo que sugiere una mejor calidad de señal en esta derivación durante el esfuerzo físico.

<img width="1316" height="899" alt="AERO_D3" src="https://github.com/user-attachments/assets/5fed8ffc-c630-4597-a7b4-28a8dac61d4e" />

**Figura 12:** Procesamiento de señal ECG con detección de picos R, cálculo de frecuencia cardíaca y promedio de latidos - Actividad aeróbica (III Derivada) escaladores. [Elaboración propia]

Se observa una frecuencia cardíaca promedio de 120.1 bpm, la más elevada de las tres derivaciones bajo esta condición, con un pico marcado de 130.5 bpm a los 2.5 s al inicio del registro, reflejando el momento de mayor intensidad justo después del ejercicio. Los picos R presentan amplitudes entre 0.5 y 0.85, y el promedio de latidos muestra ondas P, Q, R, S y T bien definidas con dispersión moderada, consistente con el patrón de recuperación cardíaca post-esfuerzo observado en las tres derivaciones.

---

## Referencias bibliográficas

[1] Y. Sattar and L. Chhabra, “Electrocardiogram,” in *StatPearls [Internet]*. Treasure Island, FL, USA: StatPearls Publishing, 2026. Available: https://www.ncbi.nlm.nih.gov/books/NBK549803/

[2] E. A. Ashley and J. Niebauer, *Cardiology Explained*. London, UK: Remedica, 2004, ch. 3, “Conquering the ECG.” Available: https://www.ncbi.nlm.nih.gov/books/NBK2214/

[3] M. Proença and K. Mrotzeck, *BITalino (r)evolution Lab Guide – Home Guide #2: Electrocardiography (ECG), Exploring Cardiac Signals at the Skin Surface*. PLUX – Wireless Biosignals, 2021. Available: https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide2_ECG.pdf

[4] J. E. Hall, *Guyton and Hall Textbook of Medical Physiology*, 14th ed. Philadelphia, PA, USA: Elsevier, 2021.

[5] S. M. Hawkins et al., “Hyperventilation-induced heart rate response as a potential marker for cardiovascular disease,” *Scientific Reports*, vol. 9, art. no. 17887, 2019. doi: 10.1038/s41598-019-54375-9.

[6] M. Stewart and A. R. Bain, “Assessment of respiratory effort with EMG extracted from ECG recordings during prolonged breath holds: Insights into obstructive apnea and extreme physiology,” *Physiological Reports*, vol. 9, no. 10, e14873, 2021. doi: 10.14814/phy2.14873.

[7] X. Bao, A. K. Abdala, and E. N. Kamavuako, “Estimation of the respiratory rate from localised ECG at different auscultation sites,” *Sensors*, vol. 21, no. 1, art. no. 78, 2021. doi: 10.3390/s21010078.

[8] J. He, Y. Kinouchi, H. Yamaguchi, and H. Miyamoto, “Exercise-induced changes in R wave amplitude and heart rate in normal subjects,” *Journal of Electrocardiology*, vol. 28, no. 2, pp. 99–106, 1995. doi: 10.1016/S0022-0736(05)80280-8.


