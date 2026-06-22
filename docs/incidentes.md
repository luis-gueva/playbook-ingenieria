# Clasificación taxonómica de Incidentes Éticos

Este módulo establece los criterios técnicos y morales para identificar, categorizar y clasificar anomalías éticas en nuestros sistemas de software.

## 📊 Taxonomía de Incidentes

| Nivel de Severidad | Tipo de Incidente | Impacto Técnico | Implicación Ética |
| :--- | :--- | :--- | :--- |
| **Crítico (P1)** | Fuga de Datos Masiva | Brecha en BD de producción | Violación de Privacidad (ACM 1.6) |
| **Alto (P2)** | Sesgo Algorítmico Activo | Discriminación en outputs de IA | Falta de Equidad (IEEE 1.4) |
| **Medio (P3)** | Opacidad de Código | Falta de documentación en decisiones | Falta de Transparencia Profesional |

## 📁 Casos de Estudio y Análisis

### Caso 01: Filtración Involuntaria por API Pública (Hipotético)
* **Descripción:** Un endpoint expone métricas de usuarios sin sanitizar tokens de identidad.
* **Análisis Técnico:** Falta de pruebas de penetración automatizadas en el pipeline de CI/CD.
* **Análisis Ético:** Vulneración del principio de confidencialidad. De acuerdo con el código de la **ACM (Sección 1.6)**, el equipo de ingeniería falló en implementar salvaguardas proporcionales al valor de los datos almacenados.

!!! info "Nota de Mitigación"
    Cualquier incidente de nivel Crítico (P1) debe activar inmediatamente el protocolo de contención detallado en la sección de [Protocolos de Respuesta](protocolos.md).

