# Manual de Ingeniería Ética

<div class="hero" markdown>
# Repositorio de buenas prácticas para la gestión de dilemas éticos

Una guía práctica para profesionales de **ingeniería informática y sistemas** que enfrentan decisiones donde la técnica no basta: hay personas, datos, derechos y consecuencias de por medio.
</div>

## ¿Para qué sirve este manual?

La ingeniería de software rara vez falla solo por errores de código. Falla cuando alguien decide **callar un riesgo conocido**, **lanzar sin probar lo suficiente**, **recolectar más datos de los necesarios** o **automatizar una decisión sin pensar en quién la sufre**.

Este repositorio reúne criterios, checklists y protocolos para que esas decisiones se tomen con cabeza fría, antes de que se conviertan en incidentes, demandas o titulares de prensa.

No es un tratado de filosofía. Es una caja de herramientas para el día a día: code reviews, despliegues, manejo de datos de usuarios, uso de IA, auditorías y respuesta a incidentes.

## Cómo está organizado

<div class="card-grid" markdown>

<div class="card" markdown>
### 📜 Fundamentos
[Código de ética](codigo-etica.md) y [buenas prácticas](buenas-practicas.md) que sostienen todo lo demás: los principios que no se negocian.
</div>

<div class="card" markdown>
### ⚠️ Gestión del riesgo
Cómo identificar y clasificar [riesgos](riesgos.md), y qué controles de [seguridad](seguridad.md) aplicar según el caso.
</div>

<div class="card" markdown>
### 🚨 Respuesta y control
[Protocolos de actuación](protocolos.md), manejo de [incidentes](incidentes.md) y [auditorías](auditorias.md) para cuando algo ya pasó (o para que no pase).
</div>

<div class="card" markdown>
### 🤖 Temas emergentes
Dilemas específicos de [inteligencia artificial](inteligencia-artificial.md): sesgos, transparencia, automatización de decisiones.
</div>

</div>

## Principios que atraviesan todo el manual

1. **El silencio también es una decisión.** No reportar un riesgo conocido es, en la práctica, decidir asumirlo en nombre de otros.
2. **La reversibilidad importa.** Ante la duda, prefiere la opción que se puede deshacer.
3. **La transparencia no es opcional con el usuario final.** Si una decisión técnica le afecta, tiene derecho a saberlo en términos que entienda.
4. **"Porque lo pidió el cliente" no es una defensa ética.** Es información, no autorización moral.
5. **La ética profesional se ejerce en equipo.** Documentar, escalar y dejar constancia protege tanto al usuario como a quien toma la decisión.

## Cómo usar este repositorio

- Si tienes un **dilema concreto entre manos**, ve directo a [Protocolos de actuación](protocolos.md): ahí hay un árbol de decisión rápido.
- Si estás **diseñando un proceso nuevo** (onboarding, code review, manejo de datos), revisa [Buenas prácticas](buenas-practicas.md).
- Si algo **ya salió mal**, ve a [Gestión de incidentes](incidentes.md).
- Si necesitas **justificar una decisión ante terceros**, el [Código de ética](codigo-etica.md) y las [Auditorías](auditorias.md) te dan el marco de referencia.

---

!!! tip "Este manual es vivo"
    Las buenas prácticas en ingeniería evolucionan con la tecnología. Si encuentras un caso que no está cubierto aquí, contribuye abriendo un *issue* o un *pull request* en el repositorio.
