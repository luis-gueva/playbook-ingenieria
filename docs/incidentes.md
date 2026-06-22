# Gestión de incidentes

## Qué cuenta como "incidente ético"

No solo brechas de seguridad. También: un sistema que discrimina sistemáticamente sin que se detectara antes, una filtración de datos por error humano, una decisión automatizada que causó daño económico a usuarios, o un patrón de diseño que resultó ser más dañino de lo previsto una vez en producción.

## Fases del protocolo de incidentes

### Fase 1 — Detección y contención

- Confirma el alcance real del incidente: qué sistemas, qué datos, cuántos usuarios.
- Detén la causa activa si es posible (desactivar una feature, revertir un despliegue, bloquear un acceso) antes de investigar a fondo. Contener primero, investigar en paralelo.
- Designa un responsable único de coordinar la respuesta, para evitar que la comunicación se disperse o se contradiga.

### Fase 2 — Evaluación de impacto

- ¿Cuántas personas están afectadas y de qué forma concreta?
- ¿El daño es reversible (se puede corregir, borrar, compensar) o irreversible (datos ya expuestos públicamente, decisión ya ejecutada con consecuencias)?
- ¿Existe obligación legal de notificación (protección de datos, normativa sectorial)?

### Fase 3 — Comunicación

**Interna primero, siempre con hechos verificados:**
Informa a quien tiene autoridad de decisión con el mayor detalle posible, evitando especulación no confirmada.

**Externa, si corresponde:**
Si hay usuarios afectados, la comunicación debe:

- Explicar qué ocurrió en lenguaje claro, sin minimizar ni usar eufemismos técnicos que oculten la gravedad real.
- Indicar qué se está haciendo para mitigar el daño.
- Indicar qué puede hacer la persona afectada (cambiar contraseña, contactar a su banco, etc.) si aplica.
- Evitar culpar a la víctima o a terceros sin evidencia confirmada.

### Fase 4 — Corrección estructural

Un incidente cerrado sin cambio estructural es un incidente que se va a repetir. Pregúntate:

- ¿Qué control faltaba que, de haber existido, habría prevenido esto?
- ¿Fue un fallo de proceso (nadie revisó), de diseño (el sistema permitía esto) o de cultura (alguien sabía y no lo reportó)?
- ¿Qué cambia, concretamente, a partir de hoy?

### Fase 5 — Documentación (post-mortem)

Todo incidente cierra con un documento que incluya:

- Cronología de hechos verificados.
- Causa raíz identificada.
- Impacto real medido (no estimado).
- Acciones correctivas con responsables y fechas.
- Lecciones aprendidas para el registro de [riesgos](riesgos.md).

!!! warning "El post-mortem no es para buscar culpables"
    Un post-mortem centrado en castigar a una persona genera el incentivo equivocado: que la próxima vez, nadie reporte un error a tiempo. El foco debe estar en el sistema y el proceso, no en la persona, salvo negligencia grave o mala fe comprobada.

## Plantilla de post-mortem

```text
Incidente: [nombre/identificador]
Fecha de detección: [fecha]
Fecha de cierre: [fecha]
Severidad: [alta/media/baja, según matriz de riesgos.md]

Cronología:
- [hora] — [evento]
- [hora] — [evento]

Causa raíz:
[Descripción técnica y de proceso]

Impacto real:
[Usuarios afectados, datos involucrados, daño económico si aplica]

Acciones correctivas:
1. [Acción] — Responsable: [nombre] — Fecha límite: [fecha]
2. [Acción] — Responsable: [nombre] — Fecha límite: [fecha]

Lecciones aprendidas:
[Qué se incorpora al registro de riesgos o a las buenas prácticas]
```

## Diferencia entre incidente y dilema

Un [dilema ético](protocolos.md) se resuelve **antes** de que ocurra el daño, evaluando opciones. Un incidente se gestiona **después**, cuando el daño ya ocurrió o está en curso. Si todavía estás a tiempo de decidir, estás en un dilema, no en un incidente — usa los [Protocolos de actuación](protocolos.md).
