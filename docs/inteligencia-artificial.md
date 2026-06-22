# Inteligencia artificial

Los sistemas de IA, especialmente los de aprendizaje automático y la IA generativa, introducen dilemas que las prácticas tradicionales de ingeniería no siempre cubren bien. Esta sección complementa, no reemplaza, el resto del manual.

## Por qué la IA necesita su propio apartado

Un sistema de IA puede:

- Tomar decisiones que ni su propio equipo de desarrollo puede explicar completamente (problema de **caja negra**).
- Reproducir y amplificar sesgos presentes en los datos de entrenamiento, incluso sin intención de quien lo construyó.
- Generar contenido (texto, imágenes, código) que se confunde con producción humana, planteando dilemas de autoría y desinformación.
- Cambiar de comportamiento con el tiempo (*drift*) sin que el código en sí haya cambiado.

## Dilemas frecuentes

<div class="dilema" markdown>
**Dilema 1 — Automatizar una decisión que antes tomaba una persona**

Un sistema de IA puede procesar miles de solicitudes (crédito, contratación, soporte) más rápido que un equipo humano. Pero, ¿qué pasa con los casos límite, donde el contexto importa más que el patrón estadístico?

**Postura recomendada:** Define explícitamente qué casos requieren revisión humana obligatoria (umbrales de confianza bajos, montos altos, categorías históricamente vulnerables a sesgo) antes de automatizar el resto.
</div>

<div class="dilema" markdown>
**Dilema 2 — Transparencia sobre el uso de IA generativa**

Un chatbot, un generador de reportes o un asistente de código puede producir contenido sin que el usuario final sepa que no fue escrito por una persona.

**Postura recomendada:** Declara cuándo el usuario está interactuando con un sistema de IA, especialmente en contextos donde la confianza en una fuente humana importa (atención al cliente, asesoría, contenido informativo).
</div>

<div class="dilema" markdown>
**Dilema 3 — Datos de entrenamiento de origen dudoso**

Usar datos recolectados sin consentimiento claro, o con licencias ambiguas, para entrenar un modelo.

**Postura recomendada:** Verifica el origen y la licencia de cualquier conjunto de datos de entrenamiento antes de su uso, igual que verificarías una dependencia de código con licencia restrictiva.
</div>

## Checklist específica para sistemas con IA/ML

- [ ] ¿Se evaluó el desempeño del modelo desagregado por subgrupos relevantes, no solo en promedio?
- [ ] ¿Existe un proceso de revisión humana para casos de baja confianza o alto impacto?
- [ ] ¿Se documentó el origen y la licencia de los datos de entrenamiento?
- [ ] ¿El usuario final sabe cuándo está interactuando con un sistema automatizado?
- [ ] ¿Existe un mecanismo de apelación si una decisión automatizada afecta negativamente a una persona?
- [ ] ¿Se monitorea el desempeño del modelo en producción para detectar deriva (*drift*)?
- [ ] ¿Se declaró el uso de IA generativa en entregables donde la autoría tiene valor contractual?

## IA generativa en el propio proceso de desarrollo

El uso de asistentes de IA para escribir código, documentación o pruebas no es, en sí mismo, un problema ético. Lo que sí lo es:

- No revisar el código generado con el mismo rigor que el código propio (la IA también introduce bugs y vulnerabilidades).
- No declarar su uso cuando la autoría tiene relevancia contractual, académica o legal (ver [Código de ética, principio 8](codigo-etica.md#8-honestidad-en-la-atribucion)).
- Confiar en explicaciones generadas por IA sobre el comportamiento de un sistema crítico sin verificación humana independiente.

## Relación con el resto del manual

- Los sesgos algorítmicos se clasifican y priorizan con la matriz de [Riesgos](riesgos.md).
- Una falla grave de un sistema de IA en producción se gestiona como cualquier otro [incidente](incidentes.md).
- La revisión periódica de sesgo y desempeño se formaliza como [auditoría](auditorias.md#auditoria-de-sesgo-algoritmico).

