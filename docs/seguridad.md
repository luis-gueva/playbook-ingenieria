# Seguridad

La seguridad informática es, en este manual, una extensión directa de la ética profesional: un sistema inseguro traslada el costo de un fallo de diseño a quien menos control tiene sobre él — el usuario final.

## Principios de seguridad con enfoque ético

### Seguridad por diseño, no por parche

Incorporar controles de seguridad desde el diseño es una decisión ética, no solo técnica: decidir "lo arreglamos después" es decidir exponer a los usuarios mientras tanto.

### El mínimo privilegio como norma, no como excepción

Cualquier persona, proceso o servicio debe tener acceso solo a lo que necesita para su función. Cada permiso adicional es una superficie de daño potencial en caso de error o compromiso.

### Cifrado de datos sensibles, en tránsito y en reposo

No es negociable para datos personales, financieros o de salud. La ausencia de cifrado en estos casos no es un descuido menor: es un riesgo trasladado al usuario sin su conocimiento.

### Gestión responsable de vulnerabilidades

Cuando se descubre una vulnerabilidad (propia o reportada por terceros):

1. No se minimiza ni se oculta ante quien debe decidir sobre el riesgo.
2. Se prioriza según impacto potencial real, no según comodidad del cronograma.
3. Se comunica a los usuarios afectados si el riesgo ya fue explotado o es significativo, siguiendo el marco de [Gestión de incidentes](incidentes.md).
4. Se documenta el proceso completo, también para protección legal del equipo.

## Controles mínimos esperables

| Control | Por qué importa éticamente |
|---|---|
| Autenticación multifactor en accesos administrativos | Reduce el daño de una sola credencial comprometida |
| Registro (logging) de accesos a datos sensibles | Permite rendir cuentas ante un incidente |
| Pruebas de penetración periódicas | Detecta riesgos antes que un atacante |
| Política de actualización de dependencias | Evita exponer a usuarios a vulnerabilidades ya conocidas y públicas |
| Plan de respuesta a incidentes documentado | Evita improvisar bajo presión, cuando se cometen más errores |
| Revisión de permisos de terceros (SDKs, APIs externas) | El riesgo de un proveedor externo se hereda al usuario final |

## Seguridad y privacidad no son lo mismo

Un sistema puede ser técnicamente seguro (sin vulnerabilidades explotables) y aun así ser invasivo de la privacidad (recolectando o compartiendo más de lo necesario). Evalúa ambos ejes por separado:

- **Seguridad**: ¿puede alguien no autorizado acceder a esto?
- **Privacidad**: ¿debería existir este dato o este acceso, aunque esté bien protegido?

## Cuándo escalar un hallazgo de seguridad

<div class="dilema" markdown>
**Dilema típico:** Encuentras una vulnerabilidad crítica dos días antes de un lanzamiento importante. El equipo de negocio presiona para lanzar igual y "parchar después".

**Postura recomendada:** Documenta el riesgo con su impacto estimado, comunícalo formalmente a quien tiene autoridad para decidir el lanzamiento, y deja constancia de tu recomendación técnica. La decisión final de negocio no es tuya, pero la responsabilidad de informar con claridad sí lo es. Ver [Protocolos de actuación](protocolos.md) para el procedimiento completo.
</div>

## Relación con otras secciones

- Para clasificar la gravedad de una vulnerabilidad como riesgo, usa la matriz en [Riesgos](riesgos.md).
- Si la vulnerabilidad ya fue explotada, sigue el proceso en [Gestión de incidentes](incidentes.md).
- Para verificar que estos controles se cumplen en el tiempo, ver [Auditorías](auditorias.md).

