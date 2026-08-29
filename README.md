<h1 style="text-align:center; color:#0077b6;">
🌪️ SIMULACIÓN DE ANIQUILACIÓN DE VÓRTICES CUÁNTICOS
<br>QUANTUM VORTEX ANNIHILATION SIMULATION 🌪️
</h1>

**ESP:** Este repositorio presenta un notebook interactivo diseñado para estudiar y visualizar la dinámica de aniquilación entre pares de vórtices y antivórtices en un fluido cuántico ideal. Mediante métodos numéricos espectrales, se analizan las condiciones físicas del condensado, el decaimiento de la energía y la emisión de fonones.

**ENG:** This repository presents an interactive notebook designed to study and visualize the annihilation dynamics of vortex–antivortex pairs in an ideal quantum fluid. Using spectral numerical methods, it analyzes the physical conditions of the condensate, energy decay, and phonon emission.

---

## 📌 Introducción / Introduction

**ESP:** El propósito principal de este notebook es modelar numéricamente el proceso de aniquilación de defectos topológicos (vórtices cuánticos) en un Condensado de Bose-Einstein (BEC). El entorno interactivo facilita la comprensión de cómo estos núcleos topológicos interactúan, colapsan y liberan energía hacia el estado base, proveyendo una herramienta robusta para la computación científica y el análisis físico.

**ENG:** The main purpose of this notebook is to numerically model the annihilation process of topological defects (quantum vortices) within a Bose-Einstein Condensate (BEC). The interactive environment facilitates understanding how these topological cores interact, collapse, and release energy into the ground state, providing a robust tool for scientific computing and physical analysis.

---

## 📌 Teoría y Metodología / Theory & Methodology

**ESP:** 
* **Ecuación de Gross-Pitaevskii (GPE):** Modela la dinámica del condensado cuántico macroscópico a temperatura cero en un régimen de campo medio, balanceando la energía cinética, el potencial de trampa armónica y las interacciones repulsivas.
* **Relajación en Tiempo Imaginario:** Convierte la propagación temporal ($dt \rightarrow -i \cdot dt$) para disipar excitaciones espurias y hacer converger el sistema hacia su verdadero estado base estable.
* **Impresión de Vórtices:** Se introduce artificialmente un perfil de fase de circulaciones opuestas (vórtice-antivórtice) y se realiza una relajación exclusiva de la densidad, formando físicamente los núcleos sin alterar su posición.
* **Detección y Energía:** Los vórtices se rastrean calculando el número de enrollamiento de la fase (integración topológica en grillas). La energía total de GPE se monitorea para registrar transiciones estructurales y disipación por ondas sonoras.

**ENG:**
* **Gross-Pitaevskii Equation (GPE):** Models the dynamics of the macroscopic quantum condensate at zero temperature in a mean-field regime, balancing kinetic energy, harmonic trap potential, and repulsive interactions.
* **Imaginary-Time Relaxation:** Converts time propagation ($dt \rightarrow -i \cdot dt$) to dissipate spurious excitations and converge the system to its true, stable ground state.
* **Vortex Imprinting:** A phase profile with opposite circulations (vortex-antivortex) is artificially introduced, followed by an amplitude-only relaxation to physically shape the cores without displacing them.
* **Detection & Energy:** Vortices are tracked by computing the phase winding number (topological grid integration). Total GPE energy is monitored to record structural transitions and dissipation via sound waves.

---

## 📌 Estructura del Notebook / Notebook Structure

**ESP:** El flujo de trabajo del documento se organiza de forma lineal y modular:
1. **Parámetros Físicos y Numéricos:** Configuración de la grilla ($N=160$), paso temporal, trampa armónica, constantes de interacción y capa absorbente para reflexiones.
2. **Relajación (Estado Base):** Ejecución del tiempo imaginario para estabilizar la nube atómica.
3. **Impresión de Vórtices:** Inyección de fase topológica y modelado del núcleo ($\sim \tanh(r/\xi)$).
4. **Detección:** Algoritmo de número de enrollamiento para ubicar posiciones espaciales precisas.
5. **Visualización Visual Setup:** Diseño de paneles simultáneos (Densidad, Fase, Campo de Velocidad, Fluctuación y Energía).
6. **Bucle de Evolución (GPE dinámica):** Propagación temporal estándar integrando factores disipativos ($\gamma$).
7. **Animación y Exportación:** Generación del registro en video interactivo o archivo `.mp4`.

**ENG:** The workflow of the document is organized linearly and modularly:
1. **Physical & Numerical Parameters:** Grid setup ($N=160$), time step, harmonic trap, interaction constants, and absorbing boundary layer.
2. **Relaxation (Ground State):** Execution of imaginary time to stabilize the atomic cloud.
3. **Vortex Imprinting:** Topological phase injection and core shaping ($\sim \tanh(r/\xi)$).
4. **Detection:** Winding number algorithm for precise spatial localization.
5. **Visual Setup:** Simultaneous panel design (Density, Phase, Velocity Field, Fluctuation, and Energy).
6. **Evolution Loop (Dynamic GPE):** Standard time propagation integrating dissipative factors ($\gamma$).
7. **Animation & Export:** Generation of interactive video record or `.mp4` file.

---

## 📌 Requisitos Técnicos y Reproducción / Technical Requirements & Reproduction

**ESP:** Para ejecutar la simulación y generar las animaciones, asegúrese de configurar el siguiente entorno:
* Lenguaje: **Python 3.8+**
* Librerías Base: `numpy` (operaciones de Fourier/FFT), `scipy.ndimage` (etiquetado de vórtices).
* Visualización: `matplotlib`, `IPython.display` (renderizado HTML en notebooks).
* *Ejecución:* Simplemente corra las celdas de manera secuencial. Es recomendable contar con al menos 4 GB de memoria RAM libre para el almacenamiento en caché de los cuadros de animación.

**ENG:** To run the simulation and generate animations, please ensure the following environment is configured:
* Language: **Python 3.8+**
* Core Libraries: `numpy` (Fourier/FFT operations), `scipy.ndimage` (vortex labeling).
* Visualization: `matplotlib`, `IPython.display` (HTML rendering in notebooks).
* *Execution:* Simply run the cells sequentially. Having at least 4 GB of free RAM is recommended to handle animation frame caching.

---

## 📌 Resultados Esperados y Relevancia Física / Expected Results & Physical Relevance

**ESP:** Tras la ejecución, se observará un estado inicial estático que rápidamente adquiere dinámica: el vórtice y antivórtice se atraen debido a los gradientes de fase locales. La visualización mostrará la paulatina aceleración de los defectos hasta que colisionan (aniquilación). En este punto de máxima tensión, el sistema liberará ondas acústicas radiales (fluctuaciones de densidad). La curva de energía del diagnóstico mostrará un decaimiento progresivo dictado por el mecanismo térmico ($\gamma$).

**ENG:** Upon execution, an initially static state will swiftly become dynamic: the vortex and antivortex will attract each other due to local phase gradients. The visualization will display the progressive acceleration of the defects until they collide (annihilation). At this point of maximum stress, the system will emit radial acoustic waves (density fluctuations). The energy diagnostic curve will exhibit a progressive decay dictated by the thermal mechanism ($\gamma$).

---

## 📌 Conclusiones / Conclusions

**ESP:** Esta simulación trasciende su naturaleza investigativa para consolidarse como un recurso fundamental en la docencia de frontera. Enseña visualmente mecánicas de fluidos cuánticos de forma palpable e integra saberes algorítmicos (solución de EDPs con Fourier) que resultan vitales en la formación integral de ciencias aplicadas y competencias digitales complejas. Resulta un cimiento excelente para comparar dinámicas bajo potenciales exóticos o rotaciones.

**ENG:** This simulation transcends its research nature to establish itself as a foundational resource in advanced teaching. It visually translates quantum fluid mechanics into a palpable form and integrates algorithmic knowledge (solving PDEs with Fourier) that is vital for comprehensive training in applied sciences and complex digital skills. It serves as an excellent baseline for comparing dynamics under exotic potentials or rotations.
