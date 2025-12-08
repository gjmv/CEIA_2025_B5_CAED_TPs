# CEIA_2025_B5_CAED_TPs

Curso de Especialización en Inteligencia Artificial  
Año 2025  
Bimestre 5  

## Materia: Computación, Algoritmos y Estructuras de Datos  

## Docente:
* Camilo Argoty

## Alumno:
* Gustavo Viñas

## TP3

### Alineación de Secuencias Genéticas mediante el Algoritmo de Needleman–Wunsch.

Enunciado: <a href="TP3/Enunciado TP3.pdf">Enunciado TP3</a>  
Documento <a href="Conceptos_teóricos.pdf">Conceptos Teóricos</a>  
Implementación del algoritmo:
* Notebook <a href="implementacion_needleman_wunsch.ipynb">implementacion_needleman_wunsch.ipynb</a>  
* Colab <a href="https://colab.research.google.com/github/gjmv/CEIA_2025_B5_CAED_TPs/blob/main/TP3/implementacion_needleman_wunsch.ipynb">implementacion_needleman_wunsch.ipynb</a>  


### Ejemplos
----
           RESULTADOS DEL ALGORITMO NEEDLEMAN-WUNSCH            

Ej. 1: GATTACA vs GCATGCU

#### 🧬 Matriz de Puntuación Completa

| | **-** | **G** | **C** | **A** | **T** | **G** | **C** | **U** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **-** | 0 | -2 | -4 | -6 | -8 | -10 | -12 | -14 |
| **G** | -2 | 1 | -1 | -3 | -5 | -7 | -9 | -11 |
| **A** | -4 | -1 | 0 | 0 | -2 | -4 | -6 | -8 |
| **T** | -6 | -3 | -2 | -1 | 1 | -1 | -3 | -5 |
| **T** | -8 | -5 | -4 | -3 | 0 | 0 | -2 | -4 |
| **A** | -10 | -7 | -6 | -3 | -2 | -1 | -1 | -3 |
| **C** | -12 | -9 | -6 | -5 | -4 | -3 | 0 | -2 |
| **A** | -14 | -11 | -8 | -5 | -6 | -5 | -2 | -1 |

Alineamiento Global Óptimo  
Secuencia 1: GATTACA  
Secuencia 2: GCATGCU

Puntaje Final del Alineamiento: -1

----------------------------------------------------------------

Ej. 2: ACGCT vs ACGTT

#### 🧬 Matriz de Puntuación Completa
| | **-** | **A** | **C** | **G** | **T** | **T** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **-** | 0 | -2 | -4 | -6 | -8 | -10 |
| **A** | -2 | 1 | -1 | -3 | -5 | -7 |
| **C** | -4 | -1 | 2 | 0 | -2 | -4 |
| **G** | -6 | -3 | 0 | 3 | 1 | -1 |
| **C** | -8 | -5 | -2 | 1 | 2 | 0 |
| **T** | -10 | -7 | -4 | -1 | 2 | 3 |

Alineamiento Global Óptimo  
Secuencia 1: ACGCT  
Secuencia 2: ACGTT

Puntaje Final del Alineamiento: 3

----------------------------------------------------------------

Ej. 3: ATGCT vs AGCT

#### 🧬 Matriz de Puntuación Completa
| | **-** | **A** | **G** | **C** | **T** |
|:---:|:---:|:---:|:---:|:---:|:---:|
| **-** | 0 | -2 | -4 | -6 | -8 |
| **A** | -2 | 1 | -1 | -3 | -5 |
| **T** | -4 | -1 | 0 | -2 | -2 |
| **G** | -6 | -3 | 0 | -1 | -3 |
| **C** | -8 | -5 | -2 | 1 | -1 |
| **T** | -10 | -7 | -4 | -1 | 2 |

Alineamiento Global Óptimo  
Secuencia 1: ATGCT  
Secuencia 2: A-GCT

Puntaje Final del Alineamiento: 2

----------------------------------------------------------------

Ej. 4: GATTACA vs GTCGACGCA

#### 🧬 Matriz de Puntuación Completa:
| | **-** | **G** | **T** | **C** | **G** | **A** | **C** | **G** | **C** | **A** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **-** | 0 | -2 | -4 | -6 | -8 | -10 | -12 | -14 | -16 | -18 |
| **G** | -2 | 1 | -1 | -3 | -5 | -7 | -9 | -11 | -13 | -15 |
| **A** | -4 | -1 | 0 | -2 | -4 | -4 | -6 | -8 | -10 | -12 |
| **T** | -6 | -3 | 0 | -1 | -3 | -5 | -5 | -7 | -9 | -11 |
| **T** | -8 | -5 | -2 | -1 | -2 | -4 | -6 | -6 | -8 | -10 |
| **A** | -10 | -7 | -4 | -3 | -2 | -1 | -3 | -5 | -7 | -7 |
| **C** | -12 | -9 | -6 | -3 | -4 | -3 | 0 | -2 | -4 | -6 |
| **A** | -14 | -11 | -8 | -5 | -4 | -3 | -2 | -1 | -3 | -3 |

Alineamiento Global Óptimo  
Secuencia 1: GATTA--CA  
Secuencia 2: GTCGACGCA

Puntaje Final del Alineamiento: -3

------------------

### Referencias utilizadas:
* <a href="documentos/COMPUTATIONAL BIOLOGY - GENOMES, NETWORKS, AND EVOLUTION.pdf">Biología Computacional - Genomas, Redes y Evolución (págs. 42-66). (Manolis Kellis et al.)</a>
* <a href="documentos/MIT6_047F15_Compiled.pdf">Computational Biology: Genomes, Networks, Evolution (págs. 25-44). (Prof. Manolis Kellis)</a>
