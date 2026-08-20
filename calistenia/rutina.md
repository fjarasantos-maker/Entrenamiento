# Rutina de entrenamiento — Calistenia + isométricos en casa

Usuario de 50 años, con molestias articulares, que sustituye el trabajo con pesos libres en gimnasio (método Bilbo, archivado en `archivo_bilbo/`) por calistenia e isométricos en casa. Motivo del cambio: el gimnasio está saturado y perder tiempo esperando banca no compensa. El gimnasio queda limitado a un día por semana, solo para lo que exige un artefacto que no hay en casa (barra baja para dominadas australianas, paralelas para fondos).

## Restricciones obligatorias (no negociables, no se sugieren ni se flexibilizan)

1. En piernas, solo isométricos. Nada de sentadilla, zancada o similar con repetición ni con explosividad — el usuario lo descartó explícitamente por su condición articular. Ejercicios permitidos: sentadilla en pared, puente de glúteo isométrico, zancada isométrica con apoyo, y variantes isométricas equivalentes.
2. El número de series de cada ejercicio es fijo, no un rango — se acordó así porque un rango generaba indecisión y tendencia a quedarse en el mínimo. Dentro de cada grupo (empuje / tracción / piernas / core), el primer ejercicio de la sesión lleva más series que el último.
3. Ningún ejercicio va al fallo. Se deja siempre margen de 2-3 repeticiones en reserva (o, en isométricos, se corta el tiempo antes de que la técnica se rompa).
4. Volumen semanal bajo por grupo muscular, adecuado a 50 años con articulaciones sensibles: en torno a 8 series de empuje, 9 de tracción, 10 de piernas y 6 de core, sumando las tres sesiones semanales. No se añaden series ni ejercicios extra para "optimizar" — es una decisión consciente del usuario, no un punto abierto.
5. Miércoles es el único día de gimnasio. Se reserva exclusivamente para los ejercicios que necesitan barra baja (dominadas australianas) o paralelas (fondos); si algún aparato está ocupado, se usa el sustituto de casa equivalente en vez de esperar.
6. Progresión: en ejercicios con repeticiones, se sube repeticiones o se avanza hacia la dominada estricta antes de añadir peso — el número de series se mantiene fijo. En isométricos, se alarga primero el tiempo de mantenimiento (p. ej. de 20 a 45 s) antes de añadir carga con las mancuernas/kettlebell — el número de series también se mantiene fijo.
7. Si aparece dolor agudo, creciente o que altera la técnica, se interrumpe el ejercicio y no se intenta compensar con más trabajo.

## Calendario semanal

| Día | Lugar | Sesión |
|---|---|---|
| Lunes | Casa | Full body — empuje + tracción + piernas isométrico + core |
| Miércoles | Gimnasio | Full body — versión con barra baja y paralelas |
| Viernes | Casa | Full body — misma sesión que el lunes |

Tres sesiones semanales, full body en las tres. No hay días de descanso intermedios asignados aparte de martes, jueves, sábado y domingo (libres).

## Sesión Lunes y Viernes — Casa

Orden dentro de cada grupo: el primer ejercicio lleva más series que el último.

| # | Ejercicio | Series fijas | Objetivo |
|---|---|---|---|
| Empuje 1 | Flexiones | 2 | 8-12 reps |
| Empuje 2 | Pike push-up isométrico | 1 | 15-25 s |
| Tracción 1 | Dead hang + negativa de dominada (barra de techo) | 2 | 15-30 s hang / 4-6 negativas |
| Tracción 2 | Remo con mancuerna a 1 mano | 1 | 10-12 reps/lado — ver carga en `material_casa.md` |
| Piernas 1 | Sentadilla en pared | 2 | 30-45 s |
| Piernas 2 | Puente de glúteo isométrico | 1 | 20-40 s |
| Piernas 3 | Zancada isométrica (apoyo en pared) | 1 | 20-30 s/lado |
| Core 1 | Plancha frontal | 1 | 30-45 s |
| Core 2 | Bird dog isométrico | 1 | 20-30 s/lado |

## Sesión Miércoles — Gimnasio

Ejercicios elegidos porque necesitan barra baja o paralelas, algo que no hay en casa (la barra de casa solo permite colgarse, no dominadas australianas).

| # | Ejercicio | Series fijas | Objetivo |
|---|---|---|---|
| Tracción 1 | Dominadas australianas (barra baja) | 2 | 10-15 reps |
| Tracción 2 | Dominadas completas / negativas (barra alta) | 1 | 4-8 reps |
| Empuje 1 | Fondos en paralelas (no bajar de 90° de codo) | 2 | 6-10 reps |
| Piernas 1 | Sentadilla isométrica (máquina/prensa) | 2 | 30-40 s |
| Piernas · sustituto si está ocupado | Sentadilla en pared | 2 | 30-45 s (no se suma aparte, es sustituto) |
| Core 1 | Plancha frontal | 1 | 30-45 s |
| Core 2 | Bird dog isométrico | 1 | 20-30 s/lado |

## Material disponible en casa

Ver `material_casa.md` para el inventario de mancuernas/discos y la referencia de carga del remo con mancuerna.

## Sistema de seguimiento (análogo al método Bilbo archivado)

Igual que en el método Bilbo, solo **un** ejercicio lleva progresión formal a la vez — el foco de mejora — mientras el resto se mantiene en el objetivo fijo definido arriba, ajustando solo por adaptación.

### Foco de mejora

El foco actual es la **negativa controlada de dominada** (tracción, lunes F1 / viernes F2), con el dead hang como calentamiento previo sin seguimiento formal. Se registra en `Progresion_calistenia.xlsx`, hoja `Ciclo`:

- Celdas amarillas = entrada manual: Fecha, Repeticiones logradas a ese tiempo objetivo, Notas.
- El resto son fórmulas — no se sobrescriben con valores fijos: el Objetivo (s) de la sesión 1 es el valor inicial configurado; cada sesión siguiente = anterior + incremento (s). Tiempo bajo tensión = Objetivo × Repeticiones. Marca estimada = Objetivo × (1 + 0,03 × Repeticiones).
- Cuando se cumpla el criterio de avance (ver `config.json` → `foco_mejora.criterio_avance`: negativa de 8 s controlada x 4 reps limpias, dos sesiones seguidas), se avisa al usuario y se abre un nuevo bloque para la siguiente fase (dominada asistida/parcial, y después dominada completa). El foco solo cambia de fase o de ejercicio cuando el usuario lo confirma, no automáticamente.
- Si en dos sesiones seguidas el resultado empeora claramente respecto a la sesión anterior (menos repeticiones al mismo objetivo, o dolor que rompe la técnica), no se sube el objetivo esa semana — se avisa y se mantiene el valor.

### Principales en mantenimiento

Los ejercicios que abren cada grupo (Flexiones, Sentadilla en pared, Plancha frontal, y en el día de gimnasio Dominadas australianas, Fondos en paralelas y Sentadilla isométrica) llevan un seguimiento simple en `config.json` → `estado_principales`: solo se anota el último resultado logrado (reps o tiempo), sin perseguir una progresión planificada. Sirve para detectar si el usuario se estanca o empeora, no para forzar subir carga.

### Secundarios

El resto de ejercicios (Pike push-up isométrico, Remo con mancuerna, Puente de glúteo, Zancada isométrica, Bird dog, Dominadas completas/negativas en barra alta) son complementarios: no se registran ni tienen reglas de progresión. El usuario ajusta la carga o el tiempo libremente cada sesión, salvo el remo con mancuerna, donde se usa `material_casa.md` como referencia de carga.

### Registro de sesiones

Las sesiones se registran en `logs/AAAA-MM.md`, un archivo nuevo por mes, con una fila por sesión.

### Hoja impresa

El usuario también lleva una hoja PDF impresa (columnas de 6 semanas) como copia física de bolsillo. Si los datos de ambos sitios difieren, preguntar cuál es el válido antes de dar por buena una progresión.
