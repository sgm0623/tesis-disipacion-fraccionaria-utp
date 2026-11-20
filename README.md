# Formulación Teórico-Experimental de la Disipación No-Local en Osciladores Viscoelásticos y Señales Biomédicas

**Trabajo de grado** — Programa de Ingeniería Física, Facultad de Ingenierías, Universidad Tecnológica de Pereira (UTP), 2026.  
**Autores:** Leonardo Esteban Ospina Uchima y Santiago Grajales Montoya.  
**Director:** Walter Serna Serna, Ph. D.

---

## Alcance y estado de la versión (`v1.0-tesis`)

Esta etiqueta marca el cierre de auditoría y organización de código/resultados asociado a la entrega de tesis (`v1.0-tesis`). El documento completo de la tesis se gestiona para su entrega formal ante la universidad, mientras que este repositorio reúne los cuadernos de procesamiento, tablas exportadas y figuras vectoriales del componente acústico/modelado.

- **Enfoque experimental y teórico:** estudio de decaimiento modal, separabilidad espectral y disipación no-local, contrastando la guitarra acústica acoplada con un banco de pruebas de monocordio sobre base de concreto de ~15 kg con las iniciales UTP.
- **Condiciones de campo:** las campañas se realizaron en distintos espacios y condiciones en Riosucio (Caldas), con recursos propios, equipos prestados y variaciones entre sesiones (distintos recintos, interfaces, micrófonos y ganancias), lo cual se declara explícitamente como limitación de comparabilidad absoluta entre campañas.
- **Banco de monocordio (puerta G1–G5 y cota en $n=1$):** sobre las 25 tomas de la cuerda Sol se ejecutó la puerta de aceptación pre-registrada (**G1–G3** satisfechos en el lote global; **G4** y **G5** global no satisfechos, con estratificación por condición en tomas de un toque y cota superior en $n=1$ para el estrato `dedo_L2`). Los ajustes de dos términos y estimaciones de $\alpha$ sobre el monocordio quedan reservados para `v1.1` / trabajo posterior a la sustentación.

---

## Estructura del repositorio

- `notebooks/`: cuadernos de Google Colab para auditoría de datos (`D1`, `D2`, `FrFT`), puerta de aceptación del monocordio (`Monocordio_Puerta_G1_G5.ipynb`) y generación de figuras (`Tesis7_figs_datos.ipynb`, `Tesis7_figs_esquemas.ipynb`, `Graficas.ipynb`).
- `results/`: tablas `.csv` exportadas (`fase0_auditoria_resultados.csv`, `ruta_R1_resultados_limpios.csv`, `D2_auditoria_ventana_extendida.csv`, `Monocordio_Puerta_G1_G5.csv`, `Monocordio_Estratos_UnToque.csv`, `Monocordio_Cota_n1.csv`).
- `fig/`: figuras vectoriales en `.pdf` utilizadas en el manuscrito.
- `README.md`: documentación general del repositorio y estado de `v1.0-tesis`.

*(Nota sobre registros de audio: los archivos `.wav` sin compresión —incluidas las tomas de D1, D2, el lote del monocordio y registros de sesión como `Pista 1_002.wav` con el comentario de Leo— no se alojan en este repositorio público y se mantienen respaldados localmente).*
