# Gestión de riesgos éticos

## ¿Qué es un "riesgo ético" en ingeniería?

Es cualquier característica del sistema o del proceso de desarrollo que pueda causar daño a una persona o grupo, **incluso si el sistema funciona exactamente como fue diseñado**. Se diferencia de un riesgo técnico clásico (caída del servicio, bug funcional) en que el sistema "funcionando bien" puede seguir siendo dañino.

## Categorías de riesgo

<span class="tag tag-alto">Alto</span> **Riesgo a la integridad física o psicológica** — sistemas de control industrial, salud, transporte, contenido dirigido a menores, mecanismos de adicción por diseño (dark patterns de retención).

<span class="tag tag-alto">Alto</span> **Riesgo a derechos fundamentales** — discriminación algorítmica, vigilancia masiva, censura no transparente, exclusión de servicios esenciales.

<span class="tag tag-medio">Medio</span> **Riesgo a la privacidad** — recolección excesiva de datos, falta de anonimización, retención indefinida, compartición con terceros sin consentimiento claro.

<span class="tag tag-medio">Medio</span> **Riesgo económico al usuario** — cobros poco transparentes, dificultar la cancelación de servicios, condiciones cambiadas sin aviso adecuado.

<span class="tag tag-bajo">Bajo</span> **Riesgo reputacional o de confianza** — errores de comunicación, inconsistencias menores entre lo prometido y lo entregado, sin daño directo medible.

## Matriz de evaluación

Para cada riesgo identificado, evalúa dos ejes:

| | **Probabilidad baja** | **Probabilidad alta** |
|---|---|---|
| **Impacto alto** | Monitorear activamente, plan de mitigación documentado | Bloqueante: no avanzar sin resolver |
| **Impacto bajo** | Aceptable con registro en el backlog | Mitigar antes de producción |

La clave está en no confundir "es poco probable" con "no importa documentarlo". Los riesgos de impacto alto se documentan siempre, sin importar la probabilidad.

## Preguntas para detectar riesgos que pasan desapercibidos

1. **¿Quién es el usuario menos favorecido por este diseño?** No el usuario promedio: el caso límite. Una persona con conexión lenta, un dispositivo viejo, una discapacidad, un idioma no soportado.
2. **¿Qué pasa si este sistema se usa a una escala 100 veces mayor?** Algunos riesgos solo aparecen con volumen (sesgo agregado, saturación de soporte, efectos de red).
3. **¿Qué pasa si los datos de este sistema se filtran?** No "si fallamos en seguridad", sino asumiendo que ya falló: ¿qué impacto tiene esa fuga concreta?
4. **¿Quién se beneficia de que este riesgo no se reporte?** Si la respuesta es "el cronograma" o "las métricas del equipo", es una señal de alerta.
5. **¿Este sistema automatiza una decisión que antes tomaba una persona?** Si es así, ¿qué garantías de revisión humana existen para los casos límite?

## Riesgos específicos por tipo de sistema

**Sistemas de recomendación / personalización**
Riesgo de polarización, cámaras de eco, explotación de vulnerabilidades psicológicas para maximizar tiempo de uso.

**Sistemas de scoring (crédito, seguros, RR.HH.)**
Riesgo de discriminación indirecta por proxies (código postal como proxy de raza o nivel socioeconómico).

**IoT y sistemas embebidos**
Riesgo de seguridad física si el dispositivo falla o es comprometido; ver también [Inteligencia artificial](inteligencia-artificial.md) si incluyen componentes predictivos.

**Plataformas con datos de menores**
Riesgo legal y ético reforzado: requiere controles de consentimiento parental, diseño sin patrones de retención adictivos, y revisión específica antes de cualquier cambio.

## Registro de riesgos

Cada proyecto debería mantener un registro vivo de riesgos éticos identificados, con: descripción, categoría, probabilidad/impacto, responsable de mitigación y estado. Este registro es además el insumo principal para una [auditoría](auditorias.md) posterior.


