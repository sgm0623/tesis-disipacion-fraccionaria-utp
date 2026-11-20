# Formulación Teórico-Experimental de la Disipación No-Local en Osciladores Viscoelásticos y Señales Biomédicas

**Trabajo de grado** — Programa de Ingeniería Física, Facultad de Ingenierías, Universidad Tecnológica de Pereira (UTP), 2026.  
**Autores:** Leonardo Esteban Ospina Uchima y Santiago Grajales Montoya.  
**Director:** Walter Serna Serna, Ph. D.  
**Versión congelada:** `v1.0-tesis` (release).

---

## 1. Qué contiene y qué no

Este repositorio reúne **cuadernos de procesamiento, tablas exportadas y figuras vectoriales**. Es el respaldo computacional verificable de la tesis.

**No contiene los registros de audio originales** (`.wav`). Estos se conservan respaldados por los autores y se facilitan bajo solicitud razonada para replicar el procesamiento. Si alguien desea solicitar los audios para replicar todo, puede escribir a **`santiago.grajales1@utp.edu.co`** o a **`santiago0623.iesa2002@gmail.com`**.

La reproducción completa de los cuadernos requiere esos registros; las tablas y figuras aquí publicadas son las salidas ya generadas y son verificables de forma independiente. El documento completo de la tesis (PDF) se reserva para su entrega formal ante la universidad y no se adjunta en este repositorio ni en el release.

---

## 2. Alcance y estado de `v1.0-tesis`

- **Objeto de estudio:** decaimiento modal de una cuerda pulsada, separabilidad espectral y disipación no-local temporal (operador de Caputo), contrastando la guitarra acústica acoplada con un banco de terminación rígida (monocordio sobre base de concreto de ~15 kg, marcado UTP).
- **Resultado central:** el orden fraccionario alfa **no es identificable** en el montaje acoplado. Se cuantifican dos obstrucciones —pared temporal y pared espectral— y se invierte el problema como espectroscopía de admitancia del puente (cota superior).
- **Condiciones de campo:** las campañas se realizaron en distintos recintos de Riosucio (Caldas), con recursos propios y equipos prestados. Interfaces, micrófonos y ganancias difieren entre sesiones; esto se declara como limitación de comparabilidad absoluta entre campañas.
- **Monocordio (D3):** sobre 25 tomas se ejecutó la puerta de aceptación pre-registrada. **G1–G3 satisfechos** en el lote global (decaimiento útil mediano 3.17 s; SNR mediano 40.0 dB; eta mínima mediana 16.6); **G4 y G5 no satisfechos** (mediana de 1 armónico sobre umbral; IQR/mediana = 1.27 global). Estratificando las tomas de un solo ataque, únicamente `dedo_L2` cumple G5 (sigma_1 = 1.1108 s^-1, IQR = 0.3051 s^-1, IQR/med = 0.275), de donde la cota **sigma_1^int <= 0.91 s^-1** y **Q^int >= 6.8e2**.
- **Reservado para v1.1 / post-sustentación:** el ajuste de dos términos sigma(omega) = a * omega^(alpha - 1) + b * omega^(1/2) y cualquier estimación de alfa con el banco de monocordio; la auditoría sobre registros ECG.

---

## 3. Estructura

notebooks/   cuadernos de auditoría, puerta de aceptación y figuras
results/     tablas CSV exportadas
fig/         figuras vectoriales PDF usadas en el manuscrito

---

## 4. Orden de ejecución

| # | Cuaderno | Entrada | Salida |
|---|---|---|---|
| 1 | `alphaCuerdaTesis_Auditoria_Limpio.ipynb` | WAV de D1 | `fase0_auditoria_resultados.csv`, `fase1_dos_escalas_identificabilidad.csv`, `ruta_R1_resultados_limpios.csv`, `tabla_admitancia_inferida_ReY.csv` |
| 2 | `alphaCuerdaTesis_Auditoria_D2.ipynb` | WAV de D2 | `D2_auditoria_ventana_extendida.csv`, `D2_ruta_R1_completo.csv`, `D2_ruta_R1_resumen_mediana_IQR.csv`, `D2_cota_R1_tarde.csv` |
| 3 | `FrFT.ipynb` | envolventes de D1 | `Fig_FrFT_Validacion_Cruzada.pdf` |
| 4 | `Monocordio_Puerta_G1_G5.ipynb` | WAV de D3 | `Monocordio_Puerta_G1_G5.csv`, `Monocordio_Estratos_UnToque.csv`, `Monocordio_Cota_n1.csv`, `Fig_C_3_Monocordio_Estratos.pdf` |
| 5 | `Tesis7_figs_datos.ipynb`, `Tesis7_figs_esquemas.ipynb`, `Graficas.ipynb` | CSV anteriores | resto de figuras del manuscrito |

`alphaCuerdaTesis.ipynb` es el **cuaderno exploratorio deprecado**. Se conserva por trazabilidad y **no debe ejecutarse** para reproducir los resultados: contiene el estimador beta retirado, cuyo diagnóstico figura en el Apéndice A del manuscrito.

---

## 5. Ambiente

Google Colab · Python 3.13.18 · NumPy 2.4.6 · SciPy 1.16.3 · Librosa 0.11.0 · Pandas 2.2.3 · Matplotlib 3.10.0.  
Manuscrito: pdfLaTeX (Overleaf), estilo bibliográfico IEEEtran.

---

## 6. Reglas de auditoría embebidas

R-N1 mediana e IQR entre repeticiones · R-N2 razón de RSS y delta AIC por muestra · R-N3 impresión de duraciones efectivas · R-N4 SNR contra piso pre-ataque · R-N5 derivación o cita para toda afirmación física · R-N6 estimador según propósito · R-N7 tablas con prosa en columnas de ancho fijo.

Los criterios de aceptación G1–G5 (monocordio) y E1–E4 (bioseñales) quedaron fijados **antes** de la inspección de los datos.

---

## 7. Cómo continuar (v1.1)

1. Repetir la campaña de monocordio con micrófono de condensador y ganancia calibrada; verificar rigidez de la base en la banda del fundamental.
2. Si G4 se satisface, ejecutar el ajuste de dos términos y reportar alfa con intervalo de confianza.
3. Test instrumentado de polarización y discriminador térmico.
4. Ejecutar la auditoría ECG bajo el protocolo pre-registrado.

---

## 8. Licencia y cita

Código bajo licencia MIT; texto, tablas y figuras bajo CC BY 4.0.

> Ospina Uchima, L. E. y Grajales Montoya, S. (2026). *Formulación Teórico-Experimental de la Disipación No-Local en Osciladores Viscoelásticos y Señales Biomédicas mediante Operadores de Cálculo Fraccionario y Ciencia de Datos*. Trabajo de grado, Ingeniería Física, Universidad Tecnológica de Pereira. Repositorio: `SGM0623/tesis-disipacion-fraccionaria-utp`, etiqueta `v1.0-tesis`.
