# Auditorías

## Por qué auditar la ética de un sistema, no solo su funcionamiento

Una auditoría técnica tradicional verifica que el sistema haga lo que dice que hace. Una auditoría ética verifica, además, si lo que hace **debería** hacerse de esa forma. Ambas son necesarias y no se sustituyen entre sí.

## Tipos de auditoría

### Auditoría de diseño (antes del despliegue)

Revisión de decisiones de arquitectura, recolección de datos y lógica de negocio antes de que el sistema llegue a producción. Es la más barata de hacer y la más efectiva, porque corrige el problema en el origen.

### Auditoría de datos (periódica)

Revisión de qué datos se están recolectando realmente (no solo lo documentado), quién tiene acceso, cuánto tiempo se conservan y si se cumple la política de retención declarada.

### Auditoría de sesgo algorítmico

Para cualquier sistema que clasifique o puntúe personas: evaluar el desempeño del sistema desagregado por grupos relevantes (género, edad, ubicación geográfica, etc.), no solo el desempeño promedio. Un modelo con 95% de precisión global puede tener 60% de precisión en un subgrupo específico.

### Auditoría de cumplimiento normativo

Verificación de que el sistema cumple con la normativa de protección de datos y sectorial aplicable (no es asesoría legal, pero sí un chequeo técnico de los controles que la normativa exige).

### Auditoría post-incidente

Se realiza después de cerrar un [incidente](incidentes.md), para verificar que las acciones correctivas prometidas efectivamente se implementaron y son efectivas.

## Qué revisar en una auditoría ética — checklist base

- [ ] **Minimización de datos**: ¿se recolecta solo lo necesario para el propósito declarado?
- [ ] **Consentimiento**: ¿el usuario sabe qué se hace con sus datos, en lenguaje claro?
- [ ] **Acceso y trazabilidad**: ¿quién puede acceder a qué datos, y queda registro de cada acceso?
- [ ] **Sesgo**: si hay clasificación de personas, ¿se evaluó por subgrupos?
- [ ] **Reversibilidad**: ¿las decisiones automatizadas con impacto en personas pueden revisarse o apelarse?
- [ ] **Documentación de riesgos**: ¿existe un registro de riesgos identificados y su estado de mitigación?
- [ ] **Plan de incidentes**: ¿existe un protocolo claro y conocido por el equipo?
- [ ] **Transparencia con stakeholders**: ¿las decisiones técnicas relevantes se comunicaron a quien debía aprobarlas?

## Quién debería auditar

| Tipo de auditoría | Auditor recomendado |
|---|---|
| Diseño | Alguien del equipo, pero no quien diseñó la feature (revisión cruzada) |
| Datos / cumplimiento | Idealmente función independiente (legal, DPO, cumplimiento) |
| Sesgo algorítmico | Equipo técnico + alguien con conocimiento del dominio social afectado |
| Post-incidente | Mezcla de equipo técnico y una persona sin responsabilidad directa en el incidente |

La auditoría puramente interna y sin independencia tiene un límite: quien diseñó el sistema tiene incentivos (conscientes o no) para no encontrar problemas graves en su propio trabajo. Cuando el riesgo es alto, busca al menos una mirada externa al equipo.

## De la auditoría a la acción

Una auditoría que no genera acciones correctivas con responsable y fecha es un ejercicio decorativo. Cada hallazgo debe registrarse con el mismo formato que un riesgo (ver [Riesgos](riesgos.md)) y darle seguimiento hasta su cierre o aceptación explícita por quien tiene autoridad para aceptar ese riesgo.

!!! tip "Frecuencia recomendada"
    Sistemas de alto riesgo (datos sensibles, decisiones automatizadas con impacto significativo): auditoría de datos y sesgo cada 6 meses como mínimo, además de cualquier auditoría de diseño antes de cambios mayores.

