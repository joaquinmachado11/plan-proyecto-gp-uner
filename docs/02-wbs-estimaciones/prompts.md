# Registro del uso de prompts

> Completar esta plantilla para dejar constancia de cómo se utilizaron herramientas de inteligencia artificial durante el trabajo.

## Datos del trabajo

- **Trabajo / proyecto:** Asistente virtual de gestión de mantenimiento controlado por voz — KIU
- **Asignatura:** Gestión de Proyectos
- **Integrantes:** Calvo, Giorgi, Machado
- **Fecha de elaboración:** 13/10/2026
- **Herramientas de IA utilizadas:** Claude Opus 5.5, Gemini Plus Avanzado, ChatGPT 5.6 Luna

## Registro de interacciones

### Interacción [N.1º]

- **Fecha:** -
- **Integrante que realizó la consulta:** Calvo, Machado
- **Herramienta y modelo:** Claude Opus 5.5, Gemini Plus Avanzado, ChatGPT 5.6 Luna
- **Etapa o actividad del trabajo:** Entrega 2
- **Objetivo de la consulta:** Estimar el esfuerzo de las tareas del proyecto
- **Contexto e información proporcionados:** EDT

#### Prompt utilizado

```text
Rol y objetivo
Asume el rol de un Project Manager con amplia y reconocida experiencia en la gestión de proyectos de productos electrónicos, particularmente en la planificación y estimación de tareas de desarrollo.
Tu objetivo es realizar una estimación de esfuerzo para cada tarea del proyecto, expresada en horas-persona (h-p).
Metodología Delphi
La estimación formará parte de un proceso Delphi compuesto por dos rondas. En este proceso participarán tres estimadores: tú y otros dos LLM considerados expertos independientes.
En esta primera ronda deberás realizar tu estimación de manera independiente, sin conocer las estimaciones de los otros participantes.
Después de la primera ronda te proporcionaré las estimaciones obtenidas de los otros participantes. Analizaremos las discrepancias relevantes y, posteriormente, realizarás una segunda estimación teniendo en cuenta la información y los argumentos discutidos.
Información disponible
El archivo adjunto contiene las tareas del proyecto. Para cada tarea se especifican:
ID de la tarea.
Descripción de las actividades a realizar.
Criterio de completitud.
Entregable asociado.
Utiliza toda esta información para estimar el esfuerzo requerido. No realices estimaciones basándote únicamente en el título de la tarea.
Criterios de estimación
Expresa las estimaciones en horas-persona (h-p), no en horas calendario.
Estima el esfuerzo necesario para completar exclusivamente la tarea indicada, considerando que sus tareas predecesoras ya fueron completadas.
No incluyas el tiempo correspondiente a tareas posteriores ni actividades que estén explícitamente definidas como tareas independientes.
Cuando exista un bloque de tareas cuya realización esté prevista para N iteraciones, realiza la estimación considerando N = 1. Es decir, estima el esfuerzo correspondiente a la ejecución de una única iteración del bloque, independientemente del número total de iteraciones previsto posteriormente en la planificación.
Excluye completamente de la estimación las tareas pertenecientes a la fase “GESTIÓN DEL PROYECTO (transversal a todas las fases)”. No asignes esfuerzo a estas tareas ni incorpores su dedicación de manera indirecta en las estimaciones de las demás tareas.
Considera las actividades necesarias para alcanzar el criterio de completitud y generar el entregable especificado.
Considera el tiempo de ejecución de actividades técnicas, análisis, diseño, implementación, documentación, pruebas y correcciones cuando correspondan a la tarea.
No supongas una jornada laboral, cantidad de personas ni calendario de trabajo, ya que se solicita esfuerzo en horas-persona, no duración calendario.
Cuando la información disponible no sea suficiente para determinar con precisión el esfuerzo, realiza supuestos razonables y explicítalos.
Mantén un criterio de estimación consistente entre todas las tareas.
No intentes aproximarte a valores "típicos", redondos o esperados por otros estimadores. Realiza la estimación según tu propio análisis de la tarea y de la información proporcionada. La finalidad de esta primera ronda es obtener estimaciones independientes para posteriormente comparar su dispersión.
Formato de respuesta
Presenta inicialmente las estimaciones en una tabla de exactamente dos columnas:
|ID de tarea|Estimación [h-p]|
|:---------:|:--------------:|
|           |                |
No agregues intervalos, valores mínimos/máximos ni estimaciones de duración calendario en esta tabla.
Después de la tabla, incluye brevemente los supuestos generales utilizados para realizar las estimaciones y señala aquellas tareas cuya estimación presente una incertidumbre particularmente elevada debido a la información disponible.

```

- **Resumen de la respuesta recibida:**
- **¿Se utilizó la respuesta?** totalmente
- **Cambios realizados por el equipo:** -
- **Verificación realizada:** -
- **Parte del trabajo en la que se incorporó:** EDT, estimaciones
- **Observaciones o limitaciones:** no se pidió la estimación de tiempos optimistas y pesimistas

### Interacción [N.2º]

- **Fecha:** -
- **Integrante que realizó la consulta:** Calvo, Machado
- **Herramienta y modelo:** Claude Opus 5.5, Gemini Plus Avanzado, ChatGPT 5.6 Luna
- **Etapa o actividad del trabajo:** Entrega 2
- **Objetivo de la consulta:** Volver a estimar el esfuerzo de las tareas del proyecto a partir de la estimación anterior
- **Contexto e información proporcionados:** EDT, respuestas de la interacción anterior

#### Prompt utilizado

```text
Rol y objetivo
Asume el rol de un Project Manager con amplia y reconocida experiencia en la gestión de proyectos de productos electrónicos, particularmente en la planificación y estimación de tareas de desarrollo.
Tu objetivo es realizar la segunda ronda de una estimación Delphi del esfuerzo de las tareas del proyecto, expresado en horas-persona (h-p).
Contexto del proceso Delphi
La estimación está siendo realizada mediante un proceso Delphi compuesto por dos rondas y cuenta con tres estimadores: tú y otros dos LLM considerados expertos independientes.
En la primera ronda, siendo el experto [], realizaste una estimación individual del esfuerzo de cada tarea sin conocer las estimaciones de los otros participantes.
Para esta segunda ronda recibirás un documento que contiene las estimaciones realizadas por los otros dos expertos en la primera ronda. Además, dispones de tu propia estimación realizada en la primera ronda dentro del contexto de esta conversación.
Debes utilizar esta información para revisar críticamente tus estimaciones de la primera ronda. El objetivo de esta ronda es determinar si corresponde mantenerlas o modificarlas a partir de las diferencias observadas y del razonamiento que pueda inferirse de las estimaciones de los otros expertos.
No debes limitarte a calcular un promedio entre las estimaciones. Realiza nuevamente el análisis de cada tarea y determina la estimación que consideres técnicamente más adecuada.
Información de las tareas
El archivo original del proyecto contiene, para cada tarea:
ID de la tarea.
Descripción de las actividades a realizar.
Criterio de completitud.
Entregable asociado.
Utiliza esta información junto con los resultados de la primera ronda para realizar la nueva estimación.
Criterios de estimación
Expresa todas las estimaciones en horas-persona (h-p), no en horas calendario.
Estima el esfuerzo necesario para completar exclusivamente la tarea indicada, considerando que sus tareas predecesoras ya fueron completadas.
No incluyas el tiempo correspondiente a tareas posteriores ni actividades que estén explícitamente definidas como tareas independientes.
Cuando exista un bloque de tareas cuya realización esté prevista para N iteraciones, realiza la estimación considerando N = 1. La estimación debe corresponder al esfuerzo de una única iteración.
Excluye completamente de la estimación las tareas pertenecientes a la fase “GESTIÓN DEL PROYECTO (transversal a todas las fases)”. No asignes esfuerzo a estas tareas ni incorpores su dedicación de manera indirecta en las estimaciones de las demás tareas.
Considera las actividades necesarias para alcanzar el criterio de completitud y generar el entregable especificado.
Considera, cuando corresponda, análisis, diseño, implementación, documentación, pruebas, integración, depuración y correcciones necesarias para completar la tarea.
No supongas una jornada laboral, cantidad de personas ni calendario de trabajo.
Mantén un criterio de estimación consistente entre todas las tareas.
Estimación de tres puntos
Para cada tarea debes proporcionar tres estimaciones de esfuerzo:
Optimista (O): esfuerzo necesario suponiendo que el desarrollo se realiza en condiciones muy favorables, sin inconvenientes relevantes, con decisiones técnicas acertadas desde el comienzo y sin retrabajos significativos.
Más probable (M): esfuerzo que consideras más probable en condiciones normales de desarrollo, contemplando las dificultades, iteraciones, verificaciones y correcciones que razonablemente pueden presentarse.
Pesimista (P): esfuerzo necesario bajo condiciones desfavorables pero plausibles, considerando que pueden presentarse dificultades técnicas, errores, retrabajos, problemas de integración, resultados insatisfactorios en pruebas u otros inconvenientes razonablemente esperables.
El valor pesimista no debe representar un escenario catastrófico o prácticamente imposible, sino un escenario desfavorable que siga siendo razonablemente plausible dentro del desarrollo del proyecto.
Debe cumplirse, para cada tarea:
O ≤ M ≤ P
Revisión de la primera ronda
Para cada tarea compara conceptualmente tu nueva estimación con:
Tu estimación de la primera ronda.
La estimación del segundo experto.
La estimación del tercer experto.
Cuando existan discrepancias importantes, analiza posibles causas tales como diferencias en la interpretación del alcance, complejidad técnica, actividades consideradas, riesgos, retrabajo o alcance del entregable.
No adoptes automáticamente la estimación de otro experto ni descartes la tuya únicamente por ser diferente. La discrepancia debe utilizarse como información para reexaminar los supuestos y el alcance de la tarea.
Formato de respuesta
Presenta inicialmente una tabla con las estimaciones definitivas de esta segunda ronda:
|ID de tarea|Optimista (O) [h-p]|Más probable (M) [h-p]|Pesimista (P) [h-p]|
|:--:|:--:|:--:|:--:|

No calcules ni agregues una estimación ponderada o esperada a menos que se solicite explícitamente.
Después de la tabla, incluye una explicación breve de:
Los criterios o supuestos generales utilizados en esta segunda ronda.
Las tareas cuya estimación fue modificada de manera significativa respecto de tu primera ronda y el motivo principal del cambio.
Las tareas que presentan una incertidumbre particularmente elevada y la razón de dicha incertidumbre.
La tabla debe contener únicamente las tareas que correspondan a la estimación del proyecto y debe excluir las tareas de “GESTIÓN DEL PROYECTO (transversal a todas las fases)”.
```

- **Resumen de la respuesta recibida:**
- **¿Se utilizó la respuesta?** parcialmente
- **Cambios realizados por el equipo:** La reestimacion de algunas tareas se descartó
- **Verificación realizada:** -
- **Parte del trabajo en la que se incorporó:** EDT, estimaciones
- **Observaciones o limitaciones:** error en la aplicación de la técnica Delphi

### Interacción [N.3º]

- **Fecha:** -
- **Integrante que realizó la consulta:** Calvo
- **Herramienta y modelo:** Claude Opus 5.5
- **Etapa o actividad del trabajo:** Realización del cronograma
- **Objetivo de la consulta:** Realizar el cronograma a partir de la red de tareas y estimacion de duración
- **Contexto e información proporcionados:** EDT, estimaciones, red de tareas

#### Prompt utilizado

```text
Elaborá el cronograma del proyecto a partir de los datos de la tabla adjunta (ID de tarea, descripción, esfuerzo en horas-persona y predecesoras).
Reglas de cálculo:
Duración (días) = esfuerzo (h-persona) / 8 h, redondeando siempre hacia
 arriba al día entero. Cada tarea la realiza una sola persona.
Se trabaja de lunes a viernes; se excluyen sábados, domingos y feriados
 nacionales de Argentina de 2027.
El proyecto comienza el lunes 01/03/2027. Las tareas sin predecesoras
 empiezan ese día.
Todas las dependencias son fin-comienzo: una tarea empieza el día hábil
 siguiente al fin de su predecesora. Si tiene varias, considerá la que
 termina más tarde.
Las tareas sin dependencia entre sí pueden ejecutarse en paralelo
 (las realizan personas distintas).
Una tarea de 1 día empieza y termina el mismo día.
Formato de salida: una tabla con las columnas
 ID de tarea | Predecesoras | Esfuerzo (h-persona) | Duración (días) | Inicio | Fin
 Fechas en formato dd/mm/aaaa.
En el archivo de excel están los datos que necesitas
```

- **Resumen de la respuesta recibida:**
- **¿Se utilizó la respuesta?** parcialmente
- **Cambios realizados por el equipo:** cambios en la graficación
- **Verificación realizada:** -
- **Parte del trabajo en la que se incorporó:** cronograma
- **Observaciones o limitaciones:** graficación poco clara


## Síntesis del uso de IA

- **Tareas para las que se utilizó IA:**
- **Aportes que se incorporaron al trabajo:**
- **Aportes que se descartaron y motivo:**
- **Controles realizados por el equipo para comprobar la calidad y exactitud:**
- **Decisiones y contenidos desarrollados por el equipo sin asistencia de IA:**

## Declaración del equipo

El equipo declara que este registro describe de manera fiel el uso de herramientas de IA en el trabajo. Las respuestas utilizadas fueron revisadas y adaptadas por sus integrantes, quienes son responsables del contenido final y de verificar su exactitud.

- **Integrantes que revisaron y validaron el contenido:** Giorgi
- **Fecha de revisión:** 13/10/2026