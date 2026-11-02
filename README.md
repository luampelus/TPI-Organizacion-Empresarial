# lagarto-pos · Trabajo Práctico Integrador

**Organización Empresarial — Tecnicatura Universitaria en Programación a Distancia (UTN)**

Documentación del Trabajo Práctico Integrador (TPI) sobre **Cerveza Lagarto Foodtruck** y su sistema de punto de venta **lagarto-pos**.

## Integrantes

| Nombre | Rol en el proyecto |
|---|---|
| Lua Manuel Pelus | Trabajo individual: análisis, documentación y desarrollo de lagarto-pos |

**Cátedra:** Prof. Gabriela Martínez (titular); Prof. Carolina Bruno, Prof. Mario Raúl López y Prof. Andrea Ramos (adjuntos).

## Enlaces

- **Repositorio:** https://github.com/luampelus/TPI-Organizacion-Empresarial
- **Tablero de gestión (GitHub Projects):** https://github.com/users/luampelus/projects/1/views/1

## Descripción del sistema

Cerveza Lagarto Foodtruck tiene dos foodtrucks, **Lagarto Parrilla** y **Lagarto Pizza**. **lagarto-pos** es el sistema de punto de venta que se usa en los dos: registra ventas, stock, mermas y cierres de caja, y manda los datos a un panel en vivo para los dueños.

La próxima etapa, planificada en la Entrega N.º 2, agrega:

- el **costo de cada producto**,
- un **reporte de ganancia por producto y por período** (ventas − costo de lo vendido − mermas),
- **acceso restringido con clave**, para que solo la Dirección (los 4 socios) y el desarrollador vean costos y ganancias.

**Tecnología:** HTML y JavaScript en una tablet con Chrome (funciona sin internet), Firebase Realtime Database para el panel en vivo y Netlify para publicarlo.

## Contenido del repositorio

| Carpeta / archivo | Contenido |
|---|---|
| [`docs/entregas/`](docs/entregas/) | Entregas N.º 1, 2 y 3 en PDF |
| [`docs/bpmn/`](docs/bpmn/) | Diagrama BPMN del proceso de venta, merma y cierre |
| [`docs/backlog/historias-de-usuario.md`](docs/backlog/historias-de-usuario.md) | Las tres historias de usuario del tablero |
| [`docs/control/indicadores.md`](docs/control/indicadores.md) | Indicadores de control y estándares de desempeño |

## Recorrido del TPI

| Entrega | Tema | Resultado principal |
|---|---|---|
| N.º 1 | La organización y su enfoque sistémico | La empresa como sistema abierto y lagarto-pos como módulo |
| N.º 2 | Diagnóstico y planeación | FODA, objetivo y metas medibles (M1 a M6), Gantt de 8 semanas |
| N.º 3 | Estructura formal y diseño de datos | Organigrama y diccionario de datos (5 entidades) |
| N.º 4 | Procesos, trabajo colaborativo y control | BPMN, este repositorio, tablero ágil e indicadores de control |

## Forma de trabajo en el repositorio

- `main` tiene siempre la versión revisada de la documentación.
- Cada cambio se hace en una **rama secundaria** (`docs/...`) y entra a `main` por **Pull Request**.
- Los mensajes de commit siguen el formato `tipo(alcance): descripción`, por ejemplo `docs(bpmn): agregar diagrama del proceso de venta`.
- Cada historia de usuario es un *issue* vinculado al tablero, con los estados **Por hacer**, **En progreso** y **Listo**.

## Declaración de Uso de IA

Usé Claude (de Anthropic) como **herramienta de apoyo** durante el TPI: para ordenar el trabajo según cada consigna, generar borradores de redacción y de diagramas, y agilizar las tareas de Git y GitHub. El análisis del caso, las decisiones del proyecto y la revisión final son míos. Abajo detallo cómo lo usé y qué corregí.

### Cómo estructuré los prompts

1. **Contexto real primero.** Partí de información real del negocio y de lagarto-pos (que desarrollo yo), y de mis entregas anteriores, para que trabajara sobre datos verificables y no inventara.
2. **Preguntas antes de redactar.** Le pedí que me consultara lo que necesitara saber (estructura de la empresa, puestos, estado del proyecto). Así el contenido refleja la organización real y no suposiciones del modelo.
3. **Revisión contra la rúbrica.** Le pedí una evaluación crítica según la rúbrica de la cátedra para detectar puntos débiles antes de entregar.

### Correcciones que hice sobre lo que generó la IA

| Entrega | Lo que propuso la IA | Lo que corregí yo |
|---|---|---|
| N.º 2 | Planteaba como proyecto nuevo el registro de mermas | Las mermas ya existían en el sistema y llegaban en vivo al panel. Cambié el proyecto a costos, ganancia por producto y acceso restringido |
| N.º 2 | En el FODA ponía como fortaleza "base para calcular ganancias" y como debilidad "no calcula ganancias" | Era una contradicción. Saqué la fortaleza |
| N.º 2 | Ponía como oportunidad que "los dueños pueden ajustar promos con datos de ganancia" | Eso es un resultado del proyecto, no algo del entorno. Lo cambié por una oportunidad externa |
| N.º 2 | Plazo de 12 semanas | Lo ajusté a 8 semanas, según mi disponibilidad real |
| N.º 2 | No mencionaba un riesgo real | Agregué que el historial y el stock se respaldan en la cuenta de Chrome y que hay que cuidar las claves |
| N.º 2 | Bibliografía con libros y ediciones que no pude verificar | La saqué para no citar fuentes posiblemente inventadas. Dejé solo los apuntes de la unidad |
| N.º 2 | En las siglas puso "dueños y encargados" | En la empresa no hay encargados formales. Lo aclaré en la Entrega 3 |
| N.º 3 | Puso "despacho de pedidos" y "ayudante de plancha" como dos puestos | Es una sola persona: Parrilla tiene 4 empleados y Pizza tiene 2 |
| N.º 3 | Reducía la barra de Parrilla a "cerveza tirada" | Los tirados también incluyen tinto y vermouth. Cambié el puesto a "barra de bebidas tiradas" |
| N.º 3 | Reparto de tareas de los socios incompleto | Agregué que un socio trae aderezos y verduras, y saqué "luces" porque no es algo recurrente |

### Lo que aporté yo

- **El caso y los datos:** la estructura de la empresa, los puestos, el funcionamiento de cada foodtruck y los problemas del día a día salen de mi trabajo en Cerveza Lagarto Foodtruck.
- **Las decisiones del proyecto:** el alcance de la próxima etapa de lagarto-pos, los plazos según mi disponibilidad real y el estado real de cada historia de usuario.
- **La validación técnica:** el asistente no tuvo acceso al código de lagarto-pos. Los campos del diccionario de datos son conceptuales y los validé contra cómo funciona el sistema que desarrollo (medios de pago, ventas editables, mermas con el botón "−").
- **La revisión:** revisé cada entrega antes de subirla y el Pull Request del BPMN antes de integrarlo. Los errores que hayan quedado son míos.
