# 🔗 Red de Tareas y Camino Crítico

## Diagrama de precedencias

> Las tareas del **Camino Crítico** se muestran en rojo (holgura = 0).

### Fase 1: Iniciación y arquitectura
```mermaid
flowchart LR
    START(["▶ INICIO"])

    T111["1.1.1 Relevamiento con técnicos del SIC\n⏱ Xd"]
    T112["1.1.2 Analizar el software KIBBO y su interfaz MCP\n⏱ Xd"]
    T113["1.1.3 Elaborar el documento de casos de uso iniciales\n⏱ Xd"]
    T114["1.1.4 Priorización de casos de uso y definición del alcance del prototipo\n⏱ Xd"]

    T121["1.2.1 Definir requisitos funcionales\n⏱ Xd"]
    T122["1.2.2 Definir requisitos no funcionales\n⏱ Xd"]
    T123["1.2.3 Elaborar la matriz de trazabilidad\n⏱ Xd"]

    T131["1.3.1 Definición de arquitectura general e interfaces\n⏱ Xd"]
    T132["1.3.2 Definición de arquitectura de hardware\n⏱ Xd"]
    T133["1.3.3 Definición de arquitectura de firmware\n⏱ Xd"]
    T134["1.3.4 Definición de arquitectura de servicios en la nube\n⏱ Xd"]
    T135["1.3.5 Definición de arquitectura de seguridad\n⏱ Xd"]

    T14["1.4 Evaluación y selección de proveedores de STT/LLM/TTS\n⏱ Xd"]

    H1{{"◆ HITO\nAprobación de la definición y diseño preliminar del proyecto"}}

    START --> T111
    START --> T112

    T111 --> T113
    T112 --> T113
    T113 --> T114

    T114 --> T121
    T114 --> T122

    T121 --> T123
    T122 --> T123

    T121 --> T131
    T122 --> T131

    T131 --> T132
    T131 --> T133
    T131 --> T134
    T131 --> T135

    T134 --> T14

    T123 --> H1
    T132 --> H1
    T133 --> H1
    T134 --> H1
    T135 --> H1
    T14 --> H1

    classDef tarea fill:#FFCCCC,stroke:#C62828,color:#000000
    classDef hito fill:#FFF2CC,stroke:#B8860B,stroke-width:2px,color:#000000
    class START,H1 hito
    class T111,T112,T113,T114,T121,T122,T123,T131,T132,T133,T134,T135,T14 tarea

```
### Fase 2: Diseño y desarrollo del prototipo
```mermaid
flowchart LR
    H1{{"◆ HITO\nAprobación de la definición y diseño preliminar del proyecto"}}

    T2111["2.1.1.1 Selección de componentes\n⏱ Xd"]
    T2112["2.1.1.2 Diseño esquemático\n⏱ Xd"]
    T2113["2.1.1.3 Diseño de PCB\n⏱ Xd"]
    T2114["2.1.1.4 Diseño del gabinete\n⏱ Xd"]
    T2115["2.1.1.5 Generación de lista de materiales y calcular el costo unitario\n⏱ Xd"]

    T2121["2.1.2.1 Diseño de módulos\n⏱ Xd"]
    T2122["2.1.2.2 Diseño de comunicación dispositivo-backend\n⏱ Xd"]

    T2131["2.1.3.1 Diseño de flujos conversacionales por caso de uso priorizado\n⏱ Xd"]
    T2132["2.1.3.2 Integración con MCP de KIBBO\n⏱ Xd"]

    T214["2.1.4 Elaborar el plan de verificación técnica\n⏱ Xd"]

    T2151["2.1.5.1 Solicitar cotizaciones y selección de proveedores\n⏱ Xd"]
    T2152["2.1.5.2 Generación de órdenes de compra\n⏱ Xd"]
    T2153["2.1.5.3 Realizar el seguimiento de envío e importación\n⏱ Xd"]
    T2154["2.1.5.4 Recepción e inspección de componentes\n⏱ Xd"]

    T216["2.1.6 Revisión de diseño\n⏱ Xd"]

    H2{{"◆ HITO\nDiseño aprobado y componentes recibidos"}}

    T2211["2.2.1.1 Fabricación y montaje de PCB\n⏱ Xd"]
    T2212["2.2.1.2 Fabricación del gabinete\n⏱ Xd"]
    T2213["2.2.1.3 Ensamble del dispositivo y pruebas eléctricas\n⏱ Xd"]

    T2221["2.2.2.1 Implementación de captura y preprocesamiento de audio\n⏱ Xd"]
    T2222["2.2.2.2 Implementación de activación y gestión de estados\n⏱ Xd"]
    T2223["2.2.2.3 Implementación de conectividad y mecanismos de seguridad\n⏱ Xd"]
    T2224["2.2.2.4 Implementación de la reproducción de audio\n⏱ Xd"]
    T2225["2.2.2.5 Ejecutar pruebas unitarias del firmware\n⏱ Xd"]

    T2231["2.2.3.1 Integrar STT, intérprete y TTS\n⏱ Xd"]
    T2232["2.2.3.2 Integración MCP con KIBBO\n⏱ Xd"]
    T2233["2.2.3.3 Implementación de los casos de uso priorizados\n⏱ Xd"]

    T2241["2.2.4.1 Integración de hardware con firmware\n⏱ Xd"]
    T2242["2.2.4.2 Integración del dispositivo con la nube y KIBBO (integración punta a punta)\n⏱ Xd"]

    T2251["2.2.5.1 Ejecutar ensayos de reconocimiento de voz con ruido y a distancia\n⏱ Xd"]
    T2252["2.2.5.2 Ejecutar ensayos de latencia y conectividad\n⏱ Xd"]
    T2253["2.2.5.3 Ejecutar ensayos de seguridad\n⏱ Xd"]
    T2254["2.2.5.4 Elaborar informe de verificación técnica\n⏱ Xd"]

    T226["2.2.6 Redacción de manual técnico y manual de usuario\n⏱ Xd"]

    H3{{"◆ HITO\nPrototipo funcional verificado"}}

    H1 --> T2111
    T2111 --> T2112
    T2112 --> T2113
    T2111 --> T2114
    T2113 --> T2115
    T2114 --> T2115

    H1 --> T2121
    T2121 --> T2122

    H1 --> T2131
    T2131 --> T2132

    H1 --> T214

    T2115 --> T2151
    T2151 --> T2152
    T2152 --> T2153
    T2153 --> T2154

    T2115 --> T216
    T2122 --> T216
    T2132 --> T216
    T214 --> T216
    T2154 --> T216

    T216 --> H2

    H2 --> T2211
    H2 --> T2212
    T2211 --> T2213
    T2212 --> T2213

    H2 --> T2221
    H2 --> T2222
    H2 --> T2223
    H2 --> T2224

    T2221 --> T2225
    T2222 --> T2225
    T2223 --> T2225
    T2224 --> T2225

    H2 --> T2231
    H2 --> T2232
    T2231 --> T2232
    T2231 --> T2233
    T2232 --> T2233

    T2213 --> T2241
    T2225 --> T2241

    T2241 --> T2242
    T2233 --> T2242

    T2242 --> T2251
    T2242 --> T2252
    T2242 --> T2253

    T2251 --> T2254
    T2252 --> T2254
    T2253 --> T2254

    T2254 --> T226
    T226 --> H3

    classDef tarea fill:#FFCCCC,stroke:#C62828,color:#000000
    classDef hito fill:#FFF2CC,stroke:#B8860B,stroke-width:2px,color:#000000
    class H1,H2,H3 hito
    class T2111,T2112,T2113,T2114,T2115,T2121,T2122,T2131,T2132,T214,T2151,T2152,T2153,T2154,T216,T2211,T2212,T2213,T2221,T2222,T2223,T2224,T2225,T2231,T2232,T2233,T2241,T2242,T2251,T2252,T2253,T2254,T226 tarea

```
### Fase 3: Validación con usuarios
```mermaid
flowchart LR
    H3{{"◆ HITO\nPrototipo funcional verificado"}}

    T311["3.1.1 Selección de los casos de uso a validar\n⏱ Xd"]
    T312["3.1.2 Definición de instrumentos de feedback\n⏱ Xd"]
    T313["3.1.3 Definición de casos de prueba y criterios de aceptación\n⏱ Xd"]
    T314["3.1.4 Coordinación del piloto con un SIC\n⏱ Xd"]

    T321["3.2.1 Ejecutar pruebas funcionales de casos de uso\n⏱ Xd"]
    T322["3.2.2 Ejecutar pruebas piloto con técnicos\n⏱ Xd"]
    T323["3.2.3 Registro de defectos, feedback y necesidades no cubiertas\n⏱ Xd"]
    T324["3.2.4 Identificación y especificación de nuevos casos de uso\n⏱ Xd"]
    T325["3.2.5 Priorización de nuevos casos de uso y solicitud de cambio a KIBBO\n⏱ Xd"]
    T326["3.2.6 Ajuste del producto (hardware, firmware y nube)\n⏱ Xd"]
    T327["3.2.7 Ejecutar las pruebas de regresión\n⏱ Xd"]

    T33["3.3 Informe de validación y feedback de usuarios\n⏱ Xd"]

    H4{{"◆ HITO\nIteración de validación completada"}}

    H3 --> T311
    T311 --> T312
    T312 --> T313
    T313 --> T314

    T314 --> T321
    T321 --> T322
    T322 --> T323
    T323 --> T324
    T324 --> T325
    T325 --> T326
    T326 --> T327

    T327 --> T33
    T327 -->|"N iteraciones"| T321

    T33 --> H4

    classDef tarea fill:#FFCCCC,stroke:#C62828,color:#000000
    classDef hito fill:#FFF2CC,stroke:#B8860B,stroke-width:2px,color:#000000
    class H3,H4 hito
    class T311,T312,T313,T314,T321,T322,T323,T324,T325,T326,T327,T33 tarea

```
### Fase 4: Documentación y cierre
```mermaid
flowchart LR
    H4{{"◆ HITO\nIteración de validación completada"}}

    T411["4.1.1 Elaborar el informe final de pruebas\n⏱ Xd"]
    T412["4.1.2 Registro de problemas presentados y soluciones\n⏱ Xd"]

    T421["4.2.1 Entrega del prototipo y los repositorios\n⏱ Xd"]
    T422["4.2.2 Realizar la demostración y capacitación\n⏱ Xd"]
    T423["4.2.3 Elaborar el acta de aceptación\n⏱ Xd"]

    H5{{"◆ HITO\nActa de aceptación firmada"}}

    T431["4.3.1 Análisis de desviaciones de alcance, tiempo y costo\n⏱ Xd"]
    T432["4.3.2 Archivar la documentación del proyecto\n⏱ Xd"]
    T44["4.4 Realizar la presentación final y reunión de cierre\n⏱ Xd"]

    END(["⏹ FIN"])

    H4 --> T411
    H4 --> T412

    T411 --> T421
    T412 --> T421

    T421 --> T422
    T422 --> T423

    T423 --> H5

    H5 --> T431
    T431 --> T432
    T432 --> T44

    T44 --> END

    classDef tarea fill:#FFCCCC,stroke:#C62828,color:#000000
    classDef hito fill:#FFF2CC,stroke:#B8860B,stroke-width:2px,color:#000000
    class H4,H5,END hito
    class T411,T412,T421,T422,T423,T431,T432,T44 tarea

```

## Análisis del Camino Crítico

| ID | Tarea | Inicio Temprano | Fin Temprano | Inicio Tardío | Fin Tardío | Holgura | ¿Crítica? |
|----|-------|:-:|:-:|:-:|:-:|:-:|:-:|
| 1.1 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | 0 | ✅ |
| 1.2 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | 0 | ✅ |
| 1.3 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [X] | ❌ |
| 2.1 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | 0 | ✅ |
| 2.2 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | 0 | ✅ |
| 2.3 | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR] | [X] | ❌ |

**Duración total del proyecto:** [COMPLETAR] días

**Camino Crítico:** `INICIO → 1.1 → 1.2 → 2.1 → 2.2 → 3.1 → 3.2 → FIN`

---

*Cátedra Gestión de Proyectos · FIUNER · 2026*
