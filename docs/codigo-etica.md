# Código de ética profesional

## Propósito

Este código establece los principios mínimos que cualquier profesional de ingeniería informática y sistemas debería sostener, independientemente del proyecto, el cliente o la presión de tiempo. No sustituye los códigos de colegios profesionales o asociaciones (como el [Code of Ethics de ACM/IEEE](https://www.acm.org/code-of-ethics)); los complementa con criterios aplicables a la práctica diaria.

## Los ocho principios

### 1. Primero, no dañar

Toda decisión técnica debe evaluarse también por su impacto humano: privacidad, seguridad física, estabilidad económica, salud mental. Un sistema que "funciona" pero expone datos sensibles o genera dependencia dañina no es un sistema exitoso.

### 2. Competencia honesta

No aceptes ni asignes tareas para las que no tienes (o tu equipo no tiene) la preparación adecuada, sin antes señalarlo explícitamente. Sobreestimar tu capacidad técnica frente a un cliente o jefe es una forma de engaño.

### 3. Transparencia con quien decide

Quien toma la decisión final (cliente, product owner, dirección) debe tener la información técnica relevante en términos que pueda entender, incluyendo riesgos y limitaciones. Ocultar complejidad para "vender" una solución es una falta ética, no solo comercial.

### 4. Privacidad por diseño

Los datos personales se recolectan, almacenan y procesan con el mínimo necesario para el propósito declarado. "Podríamos necesitarlo después" no es una justificación válida para recolectar de más.

### 5. Responsabilidad sobre el código que se firma

Quien aprueba un *merge*, despliega a producción o firma una auditoría asume responsabilidad sobre las consecuencias razonablemente previsibles de esa acción, incluso si la tarea fue delegada o automatizada.

### 6. No discriminación algorítmica

Los sistemas que clasifican, puntúan o filtran personas (crédito, contratación, contenido, acceso a servicios) deben evaluarse activamente por sesgos contra grupos protegidos, no solo por exactitud promedio.

### 7. Deber de alertar

Si identificas un riesgo grave (de seguridad, legal, de daño a terceros) y no es tu decisión resolverlo, tienes la obligación de comunicarlo formalmente a quien sí puede decidir. El silencio informado es complicidad.

### 8. Honestidad en la atribución

No te atribuyas trabajo ajeno (código, diseño, ideas), ni atribuyas a otros decisiones que tomaste tú. Esto incluye el uso no declarado de herramientas de IA generativa en entregables donde la autoría importa.

## Relación entre principios y conflictos típicos

| Principio | Conflicto típico con... |
|---|---|
| Transparencia con quien decide | Presión comercial por "no asustar al cliente" |
| Privacidad por diseño | Métricas de negocio que premian más datos |
| Deber de alertar | Jerarquía organizacional / miedo a represalias |
| No discriminación algorítmica | Plazos de entrega que no contemplan auditoría de sesgo |

Estos conflictos no tienen una respuesta automática. Para resolverlos en la práctica, ve a [Protocolos de actuación](protocolos.md).

## Lo que este código no es

- No es una lista de prohibiciones técnicas (eso está en [Seguridad](seguridad.md) y [Buenas prácticas](buenas-practicas.md)).
- No sustituye el marco legal vigente (protección de datos, propiedad intelectual, normativa sectorial).
- No resuelve dilemas por ti: te da criterios para argumentar una decisión defendible.

!!! note "Sobre la exigibilidad"
    Este código es una guía de autorregulación profesional. Su valor está en que un equipo lo adopte explícitamente y lo use como referencia común, no en su capacidad de sanción.

