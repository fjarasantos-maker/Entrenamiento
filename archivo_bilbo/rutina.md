# Rutina de entrenamiento — Método Bilbo adaptado

Usuario de 50 años, mala recuperación, dolor articular general. Prioridad: adaptabilidad y sostenibilidad por encima de rendimiento máximo.

## Restricciones obligatorias (no negociables, no se sugieren ni se flexibilizan)

1. Ningún ejercicio de patrón de cadera/bisagra (peso muerto, RDL, hip thrust, pull-through) — dolor lumbar.
2. Ningún ejercicio libre de pierna, salvo la excepción explícita de abajo.
3. Excepción autorizada: media sentadilla tras nuca con barra, con rango limitado por los topes de seguridad del rack (el usuario decidió conservar este ejercicio de forma consciente pese a ser libre).
4. La serie Bilbo nunca se hace al fallo. RIR 1-3 según el ejercicio.
5. No añadir ejercicios "de relleno" sin una razón funcional explicable.

## Tipos de ejercicios

### Principal / Bilbo

Es el ejercicio que define la sesión. Se registran la carga o asistencia y las repeticiones de sus series para ajustar el entrenamiento y observar la evolución.

Cada principal puede estar en uno de estos dos modos:

- **Mejora:** es el único grupo prioritario del bloque. Realiza entre uno y tres ciclos Bilbo consecutivos usando la tabla de seguimiento.
- **Mantenimiento:** utiliza una carga o asistencia que permita aproximadamente 25 repeticiones. La carga puede cambiar por adaptación, pero no se persigue una mejora planificada.

### Secundario

Es trabajo complementario y no determina la progresión del plan. No se registran sus pesos ni repeticiones y no tiene reglas de progresión. El usuario ajusta su carga en cada sesión según cómo se encuentre, manteniendo buena técnica y sin llegar al fallo.

## Regla de calendario

Se entrenan cinco días consecutivos con sesiones deliberadamente cortas:

- El grupo en modo **mejora** ocupa siempre **martes (F1)** y **viernes (F2)**.
- F1 y F2 forman parte del mismo ciclo Bilbo: cada una avanza una sesión y un incremento en la tabla.
- Los otros tres grupos, en mantenimiento, se reparten una vez cada uno entre lunes, miércoles y jueves.
- Cuando cambia el grupo prioritario, se rehace el calendario semanal para aplicar esta misma regla y reducir en lo posible la interferencia entre grupos.

## Calendario actual — foco Pecho

| Día | Grupo | Principal / Bilbo (con seguimiento) | Secundario (sin seguimiento) |
|---|---|---|---|
| Lunes | Pierna | Media sentadilla tras nuca (rango limitado por topes de seguridad) | Curl femoral en máquina, 2×12-15 |
| Martes | Pecho — mejora F1 | Press banca | Aperturas en polea o press inclinado ligero, 2×10-12 |
| Miércoles | Espalda | Dominada asistida en máquina | Remo en polea, 2×10-12 |
| Jueves | Hombro | Press militar de pie con barra | Face pull en polea, 2×12-15 |
| Viernes | Pecho — mejora F2 | Press banca | Aperturas en polea o press inclinado ligero, 2×10-12 |

**Frecuencia:** 2 sesiones semanales para el grupo prioritario y 1 para cada grupo en mantenimiento.

**Cada sesión:** debe ser corta. Mantiene la secuencia calentamiento específico → serie Bilbo del principal → series convencionales previstas → secundario sin seguimiento. No se añade trabajo extra.

## Foco de mejora y rotación

Solo un principal está en modo mejora cada vez. El foco actual es **Pecho — Press banca**. El siguiente foco previsto es **Hombro — Press militar**, aunque la rotación definitiva la decide el usuario al terminar el bloque.

El grupo prioritario realiza un bloque de entre uno y tres ciclos Bilbo a frecuencia 2. F1 se hace el martes y F2 el viernes; ambas avanzan consecutivamente por las sesiones de la tabla. Cuando termina el bloque, ese ejercicio pasa a mantenimiento y otro principal pasa a mejora. La tabla y el calendario semanal se rehacen ajustando ejercicio, 1RM inicial, incremento y fechas al nuevo foco.

Los otros tres principales permanecen en mantenimiento. También se registran su carga o asistencia y repeticiones, pero los ajustes solo sirven para conservar una serie cercana a 25 repeticiones, no para provocar una progresión.

Los secundarios no llevan seguimiento ni progresión.

**Ciclo del principal en mejora:**
- Empieza en ~50% del 1RM vigente.
- Cada sesión F1/F2 aumenta una cantidad adaptada al ejercicio y a los discos disponibles. Para el foco actual de press banca se usan 2 kg; al rotar el grupo se recalcula.
- El usuario registra las repeticiones logradas dos veces por semana (con RIR 1-3 respetado).
- El ciclo se cierra el día que no llegue a 15 repeticiones manteniendo las reservas.
- Al cerrar: vuelve al peso inicial del ciclo (~50% del 1RM actualizado). El objetivo del nuevo ciclo es superar las repeticiones logradas en la primera semana del ciclo anterior con ese mismo peso de partida.

## Autorregulación simple

No se usa un semáforo ni se registra una valoración subjetiva del día. El usuario realiza las series que pueda con buena técnica y sin llegar al fallo. Si necesita hacer menos repeticiones o bajar el peso, registra el resultado real; la evolución de cargas y repeticiones mostrará por sí sola el estado de recuperación.

Si aparece dolor agudo, creciente o que altera la técnica, se interrumpe el ejercicio y no se intenta compensar con más trabajo.

## Archivo de seguimiento: `Progresion_bilbo_V13.xlsx`

Hoja **Ciclo**, estructurada en bloques de 17 sesiones (un bloque por ciclo, hasta 3 ciclos en paralelo en la misma hoja).

- Celdas amarillas = entrada manual del usuario: Nombre del ejercicio, 1RM INICIO, INCREMENTO (en kg), y la columna Repeticiones de cada sesión.
- El resto son fórmulas — no se sobrescriben con valores fijos:
  - PESO de la sesión 1 = 50% de 1RM INICIO; cada sesión siguiente = anterior + INCREMENTO.
  - Trabajo = PESO × Repeticiones.
  - 1RM estimado = PESO × (1 + 0,03 × Repeticiones).
  - Fila de acumulados: suma de reps y de trabajo del bloque.
  - Récord Trabajo / Récord 1RM: máximos del bloque.
- Configuración actual para el foco Press banca: 1RM INICIO = 80 kg (sesión 1 = 40 kg), INCREMENTO = 2 kg. Las sesiones alternan martes (F1) y viernes (F2), empezando el 11 de agosto de 2026.
- Cuando se cierre un ciclo (repeticiones < 15 con RIR respetado), el siguiente ciclo del bloque comienza en la siguiente sesión disponible —martes o viernes—. Su 1RM inicial se recalcula a partir del mejor 1RM estimado del ciclo anterior.
- Tras completar el bloque de entre uno y tres ciclos, la tabla se prepara para el siguiente principal en modo mejora con parámetros propios; nunca se copian los pesos de la tabla de referencia externa.

## Notas técnicas de seguridad

- En la sentadilla tras nuca, usar siempre los topes de seguridad del rack colocados a la profundidad exacta de corte, para no depender del cálculo manual en fatiga.
- Si en algún momento la posición de la barra tras nuca genera molestia de hombro (independiente del tema de rodilla/cadera), la alternativa es mover la barra a la posición delantera (sentadilla frontal) o alta a la espalda (high-bar), sin cambiar el resto de la lógica del ejercicio.
