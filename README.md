# Entrenamiento

Repositorio para hacer seguimiento de mis entrenamientos de gimnasio, pensado para usarse conversacionalmente con Claude (por ejemplo, desde el móvil en el propio gimnasio).

## Cómo funciona

1. Al empezar una sesión ("empiezo entreno"), Claude lee [`rutina.json`](rutina.json) para saber qué día de rutina toca y [`config.json`](config.json) para saber el peso actual de cada ejercicio (según la última progresión registrada).
2. Claude indica el ejercicio y el peso sugerido.
3. El usuario indica las repeticiones conseguidas por serie.
4. Claude registra la sesión en el log del mes correspondiente (`logs/AAAA-MM.md`) y actualiza `config.json` según la regla de progresión.

## Estructura

```
entrenamiento/
├── README.md          # este archivo
├── rutina.json         # plan de entrenamiento por días de la semana
├── config.json         # estado actual de progresión (peso por ejercicio, última sesión)
└── logs/
    └── AAAA-MM.md       # log de sesiones, uno nuevo por mes
```

## Importante

Los archivos `config.json` y `logs/*.md` **no se editan manualmente**: se actualizan a través de la conversación con Claude durante o después de cada sesión de entrenamiento. La lógica de progresión (cálculo automático del siguiente peso/ejercicio y validación del log) se implementará más adelante con Claude Code sobre este mismo repositorio.
