# Entrenamiento

Repositorio para hacer seguimiento de mis entrenamientos de gimnasio, pensado para usarse conversacionalmente con Claude (por ejemplo, desde el móvil en el propio gimnasio).

## Cómo funciona

1. Al empezar una sesión ("empiezo entreno"), Claude lee [`asistente.md`](asistente.md), [`rutina.md`](rutina.md) / [`rutina.json`](rutina.json) y el foco actual de [`config.json`](config.json) para saber qué día toca. Se entrenan cinco días con sesiones cortas. El grupo prioritario siempre ocupa martes (F1) y viernes (F2); los otros tres grupos se reparten entre lunes, miércoles y jueves.
2. Todos los principales/Bilbo llevan seguimiento, pero solo uno está en modo **mejora**. El principal prioritario completa un bloque de uno a tres ciclos en [`Progresion_bilbo_V13.xlsx`](Progresion_bilbo_V13.xlsx); los demás quedan en **mantenimiento**, buscando aproximadamente 25 repeticiones.
3. El usuario indica el peso o asistencia y las repeticiones de las series del principal. Claude registra el ejercicio de mejora en el xlsx y los principales de mantenimiento en `config.json` y el log mensual. Los secundarios no se registran ni progresan.
4. Cada sesión F1 o F2 avanza una posición del ciclo Bilbo. Cuando el principal de mejora baja de 15 repeticiones con las reservas respetadas, se cierra ese ciclo. Al rotar el foco se genera también un calendario semanal nuevo.

## Estructura

```
entrenamiento/
├── README.md                    # este archivo
├── asistente.md                  # cómo debe comportarse Claude en este proyecto
├── rutina.md                     # plan completo: restricciones, calendario y progresión
├── rutina.json                   # versión estructurada de rutina.md para lectura conversacional
├── Progresion_bilbo_V13.xlsx     # hasta 3 ciclos del principal actualmente en mejora
├── config.json                   # foco actual y estado de los principales en mantenimiento
└── logs/
    └── AAAA-MM.md                 # log de sesiones, uno nuevo por mes
```

## Importante

Los archivos `config.json`, `Progresion_bilbo_V13.xlsx` y `logs/*.md` **no se editan manualmente**: se actualizan a través de la conversación con Claude durante o después de cada sesión de entrenamiento. Los cambios a la rutina en sí (`rutina.md` / `rutina.json`) o a las reglas de comportamiento (`asistente.md`) son decisiones del usuario, y Claude no las propone por iniciativa propia.
