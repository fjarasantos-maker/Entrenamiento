# Entrenamiento

Repositorio para hacer seguimiento de mis entrenamientos, pensado para usarse conversacionalmente con Claude.

## Rutina activa: calistenia + isométricos en casa

Desde el 20/08/2026, sustituye al método Bilbo con pesos libres en gimnasio (saturación de banca / falta de tiempo). Tres sesiones semanales full body: lunes y viernes en casa, miércoles en el gimnasio (solo para lo que exige barra baja o paralelas).

## Cómo funciona

Sistema de seguimiento análogo al método Bilbo archivado: solo un ejercicio (el foco de mejora) lleva progresión formal a la vez; el resto se mantiene en su objetivo fijo.

1. Claude lee [`asistente.md`](asistente.md), [`rutina.md`](rutina.md) / [`rutina.json`](rutina.json) y [`material_casa.md`](material_casa.md) para saber la sesión del día y cómo dosificar carga en los ejercicios con mancuerna.
2. El foco de mejora actual — negativa controlada de dominada — se registra en [`Progresion_calistenia.xlsx`](Progresion_calistenia.xlsx), hoja `Ciclo`, igual que el Bilbo pero con segundos en vez de kilos.
3. Los principales en mantenimiento (Flexiones, Sentadilla en pared, Plancha frontal, y en el día de gimnasio Dominadas australianas, Fondos en paralelas, Sentadilla isométrica) anotan solo su último resultado logrado en `config.json` → `estado_principales`, sin progresión planificada.
4. Los secundarios no llevan seguimiento; el usuario ajusta su carga o tiempo libremente cada sesión.
5. Las sesiones se registran en `logs/AAAA-MM.md`, un archivo nuevo por mes.
6. El usuario también lleva una hoja PDF impresa como copia física — si los datos no coinciden con este repositorio, hay que preguntar cuál es la fuente válida.
7. Las restricciones (piernas solo isométrico, series fijas, volumen semanal bajo, miércoles único día de gimnasio) son decisiones ya tomadas por el usuario — Claude no las propone ni las flexibiliza por iniciativa propia.

## Estructura

```
entrenamiento/
├── README.md                    # este archivo
├── asistente.md                  # cómo debe comportarse Claude en este proyecto
├── rutina.md                     # plan completo: restricciones, calendario y progresión
├── rutina.json                   # versión estructurada de rutina.md para lectura conversacional
├── material_casa.md              # inventario de mancuernas/discos en casa y referencia de carga
├── config.json                   # rutina activa, foco de mejora y estado de los principales en mantenimiento
├── Progresion_calistenia.xlsx    # progresión formal del foco de mejora (negativa controlada de dominada)
├── hoja_seguimiento_entrenamiento.pdf  # hoja imprimible (copia física de bolsillo)
├── logs/
│   └── AAAA-MM.md                 # log de sesiones, uno nuevo por mes
└── archivo_bilbo/                 # sistema anterior (pesos libres, método Bilbo), conservado por si se retoma
    ├── README.md
    ├── asistente.md
    ├── rutina.md
    ├── rutina.json
    ├── config.json
    ├── Progresion_bilbo_V13.xlsx
    └── logs/
        └── 2026-08.md
```

## Importante

`config.json` y `logs/*.md` no se editan manualmente: se actualizan a través de la conversación con Claude. Los cambios a la rutina en sí (`rutina.md` / `rutina.json`) o a las reglas de comportamiento (`asistente.md`) son decisiones del usuario, y Claude no las propone por iniciativa propia.
