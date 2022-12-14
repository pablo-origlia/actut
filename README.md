# Automated Calibration Tool UT

## Esquema básico

La configuración del sistema está determinado por el siguiente esquema, puede dividirse en dos grupos, la parte de control que será articulada por la `PC` vinculada a todos los demás dispositivos y la parte de TEST propiamente ducha que está formada por el dispositivo bajo prueba `DUT`, el generador de señales `GEN` encargado de la exitación y el osciloscopio `ORC` para el registro de las mediciones y verificacion.

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
excludes weekdays 2022-10-21

section Estado del arte
Inicio                :done,    des1, 2022-10-20, 2022-10-21
Esboso incial         :active,  des2, 2022-10-21, 10d
Comunicación PC-ORC   :         des3, after des2, 15d
Comunicación PC-GEN   :         des4, after des3, 25d
Comunicación PC-DuT   :         des5, after des4, 35d
```
