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

Usé un asistente de IA (Claude, de Anthropic) durante todo el TPI. Abajo explico qué le pedí, por qué lo pedí así y qué corregí yo.

### Cómo armé los prompts

1. **Le di datos reales en vez de pedirle que inventara.** Le pasé la consigna, la plantilla, las entregas anteriores y el contexto de lagarto-pos (que desarrollo yo). Por ejemplo: *"Todo el contexto de lagarto-pos está en otro chat… podés verlo?"* y, para la Entrega 4, *"Me ayudás con la entrega del TPI 4? Te adjunto los archivos necesarios"*.
2. **Le pedí que me preguntara antes de escribir.** En la Entrega 2 le propuse: *"En vez de que revise todo al final, ¿querés preguntarme lo que necesites saber?"*. En la Entrega 3 me preguntó cómo están organizados los socios, si hay encargados y qué puestos hay. Así el contenido sale de la empresa real y no de suposiciones del modelo.
3. **Le pedí que se evaluara con la rúbrica.** Por ejemplo: *"Si fueses la profe, ¿cuánto me ponés?"*. Lo usé para encontrar puntos débiles, no como nota real.
4. **Pedí cambios puntuales de redacción.** Por ejemplo: *"Esas palabras me suenan poco natural"*, para que el texto suene como escribo yo.

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
| Todas | Frases poco naturales ("negocio gastronómico", "cruzando los cuadrantes", "insumos") | Las reemplacé por cómo hablamos en el negocio: "foodtrucks", "mercadería" |

### Qué no hizo la IA

- No tuvo acceso al código de lagarto-pos. Los campos del diccionario de datos son **conceptuales** y los validé contra cómo funciona el sistema (medios de pago, ventas editables, mermas con el botón "−").
- No decidió el proyecto, los plazos, la estructura de la empresa ni los datos operativos. Eso sale de mi trabajo en los foodtrucks.
- Los errores que hayan quedado son míos: revisé cada entrega antes de subirla.
