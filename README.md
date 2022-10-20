# Automated Calibration Tool UT

## Esquema básico

La configuración de setup del sistema está determinado por el siguiente esquema, puede dividirse en dos grupos, la parte de control que será articulada por la `PC` y la parte de TEST que está formada por el dispositivo bajo prueba `DUT`, el generador de señales `GEN` encargado de la exitación y el osciloscopio `ORC` para el registro de las mediciones y verificacion.

```mermaid
flowchart LR
    subgraph Test
      direction RL
      GEN --> DuT --> ORC
    end

    PC <-- LAN --> GEN
    PC <-- USB --> DuT
    PC <-- LAN --> ORC
```

## Tareas básicas

```mermaid
gantt
dateFormat  YYYY-MM-DD
title Tareas básicas para el desarrollo del ACTUT
excludes weekdays 2014-01-10

section A section
Inicio                :done,    des1, 2022-10-20, 2022-10-31
Esboso incial         :active,  des2, 2022-10-09, 3d
Comunicación PC-ORC   :         des3, after des2, 5d
Comunicación PC-GEN   :         des4, after des3, 5d
Comunicación PC-DuT   :         des5, after des4, 5d
```
