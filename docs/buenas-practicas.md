# Buenas prácticas

Prácticas concretas, organizadas por momento del ciclo de vida del software. Cada una responde a un dilema ético recurrente, no solo a una preferencia técnica.

## Diseño y planificación

- **Define el propósito del dato antes de recolectarlo.** Si no puedes explicar en una frase por qué necesitas un campo de datos, no lo pidas.
- **Documenta las decisiones de diseño con trade-offs explícitos**, especialmente cuando una opción es más barata pero menos segura o menos privada.
- **Incluye a alguien fuera del equipo técnico en la revisión de features sensibles** (datos de menores, salud, finanzas, ubicación).

<div class="dilema" markdown>
**Dilema típico:** El cliente pide geolocalización "por si la necesitamos después" para una app que no la requiere hoy.

**Postura recomendada:** No implementarla hasta que exista un caso de uso concreto. Recolectar "por si acaso" traslada el riesgo de privacidad al usuario sin beneficio actual para él.
</div>

## Desarrollo y revisión de código

- **El code review no es solo de estilo y bugs**: incluye una pregunta explícita de "¿este cambio introduce un riesgo de seguridad, privacidad o sesgo?".
- **Ningún cambio a producción sin segundo par de ojos**, sin excepción por urgencia. Las excepciones de urgencia son exactamente donde se cuelan los errores graves.
- **Declara el uso de IA generativa en el código** cuando una porción significativa proviene de ella, especialmente en proyectos donde la autoría tiene valor contractual o legal.

## Manejo de datos

- **Minimización**: recolecta lo mínimo, conserva lo mínimo, accede lo mínimo.
- **Anonimización real, no superficial**: quitar el nombre no anonimiza si quedan suficientes campos para re-identificar a la persona (código postal + fecha de nacimiento + género ya es identificable en la mayoría de poblaciones).
- **Acceso con registro (logging)**: cualquier acceso a datos sensibles debe quedar trazado, incluyendo accesos de soporte o administración interna.
- **Plan de retención y borrado**: define desde el diseño cuándo y cómo se eliminan los datos que ya no se necesitan.

## Despliegue y operación

- **Feature flags para cambios de alto impacto**, que permitan revertir sin necesidad de un nuevo despliegue.
- **Comunicación proactiva de incidentes a usuarios afectados**, no solo cuando la ley lo exige sino cuando el daño potencial lo justifica.
- **Monitoreo de deriva (drift) en sistemas con componentes de IA o reglas de negocio automatizadas**, para detectar cuándo el comportamiento real se aleja del esperado.

## Relación con clientes y stakeholders

- **Pon los riesgos por escrito**, aunque ya los hayas mencionado en una reunión. Un correo o un documento compartido es prueba; una conversación verbal no.
- **No prometas plazos que sabes que obligarán a saltar pruebas de seguridad o privacidad.** Si la presión viene de arriba, la responsabilidad de comunicar el riesgo sigue siendo tuya.
- **Aclara expectativas sobre propiedad y uso de datos** antes de empezar, no al final del proyecto.

## Checklist rápida antes de un despliegue sensible

- [ ] ¿Se evaluaron los datos personales involucrados y su minimización?
- [ ] ¿Existe un plan de rollback?
- [ ] ¿Se comunicaron los riesgos conocidos a quien aprueba el despliegue?
- [ ] ¿Hay logging suficiente para investigar un incidente si ocurre?
- [ ] ¿Se revisó el sistema por sesgos si involucra clasificación de personas?
- [ ] ¿Hay un responsable claro si algo falla en producción?

Si alguna casilla queda sin marcar y el despliegue sigue adelante, esa decisión debería quedar documentada y firmada por quien la autoriza — ver [Protocolos de actuación](protocolos.md).

