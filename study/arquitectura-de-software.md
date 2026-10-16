# Plan de estudio: arquitectura de software y decisiones de diseño

Study depth: heavy

## Objetivo y alcance

Comprender los mecanismos que componen una arquitectura y desarrollar criterio
para elegirlos, combinarlos, evaluarlos y revisarlos cuando cambia el contexto.
El recorrido conserva la cobertura del examen y agrega fundamentos necesarios
para transferir el razonamiento a sistemas de trabajo y a casos nuevos.

El alcance incluye las familias de soluciones presentes en la materia y los
fundamentos de comunicación, datos, seguridad y operación que permiten
analizarlas. Los productos concretos funcionan como ejemplos verificables de
esas familias. La especialización administrativa de cada producto queda para
estudios posteriores según una necesidad concreta.

Los bloques 2 a 4 establecen una base explícita de atributos de calidad. Los
bloques posteriores retoman esos atributos al comparar alternativas. El orden
sigue dependencias; cada bloque puede requerir varias sesiones breves.

## Dinámica y criterios de cobertura

- Investigar el bloque a la profundidad guardada antes de enseñarlo, siguiendo
  sus fuentes y contrastando los detalles que afecten la decisión.
- Trabajar problema, intuición, mecanismo, supuestos, alternativas, costos,
  limitaciones, casos límite y condiciones para revisar una elección.
- Utilizar un caso conductor inventado: una plataforma de reservas con cupos
  limitados, pagos y notificaciones. Introducir requisitos gradualmente. Usar
  también telemetría y una aplicación interna para practicar transferencia.
- Pedir una justificación antes de mostrar una solución y hacer preguntas
  numeradas. Esperar el razonamiento del estudiante y discutirlo antes de avanzar.
- Proponer experimentos pequeños cuando permitan comprobar un supuesto
  relevante. Su ejecución se acuerda durante el estudio; este mapa no implementa
  un sistema ni constituye un plan de resolución de una práctica.
- Cerrar cada bloque con una explicación del mecanismo, una elección defendida,
  una alternativa razonable y un cambio de contexto que altere la elección.
- Considerar un bloque cubierto después de la explicación y la discusión,
  cuando no queden confusiones importantes. Las preguntas pendientes mantienen
  el estado actual. Guardar aquí solamente los estados de cobertura.

## Bloques

1. [in progress] Arquitectura, contexto y requisitos significativos
   - **Alcance:** decisiones estructurales y de comportamiento; límites del
     sistema, stakeholders, requerimientos funcionales, atributos de calidad y
     restricciones. ASR, supuestos, incertidumbre, costo, plazos y ciclo
     arquitectura-negocio. Distinguir componente conceptual, módulo, proceso,
     servicio y nodo sin exigir todavía sus implementaciones.
   - **Resultados:** delimitar un sistema y sus dependencias; identificar qué
     requisitos obligan a tomar decisiones relevantes; justificar la influencia
     del negocio y de las capacidades del equipo.
   - **Preguntas y práctica:** construir una primera descripción de reservas;
     clasificar requisitos y explicar cómo cambiaría el diseño si cambian.
   - **Fuentes:** [arquitectura](../wiki/topics/arquitectura-de-software.md),
     [ciclo arquitectura-negocio](../wiki/topics/ciclo-arquitectura-negocio.md);
     [OFF-013](../sources/extracted/OFF-013.md), pp. 2-10, 13, 22-24;
     [OFF-019](../sources/extracted/OFF-019.md), pp. 6-7;
     [EXT-001](../sources/extracted/EXT-001.md), «Introducción a la Arquitectura
     de Software» y «Architecture-Business Cycle (ABC)».

2. [pending] Atributos de calidad de ejecución
   - **Alcance:** disponibilidad, confiabilidad, tolerancia a fallos, rendimiento,
     escalabilidad, interoperabilidad, administrabilidad, personalización,
     precisión, auditabilidad y seguridad. Distinguir latencia de throughput y
     capacidad de escalabilidad; reconocer la perspectiva del usuario y los
     diferentes alcances de las definiciones docentes.
   - **Resultados:** explicar cada atributo con un ejemplo y un contraejemplo;
     diferenciar disponibilidad, confiabilidad y tolerancia a fallos; reconocer
     cuáles son relevantes en sistemas transaccionales y de sensores. Relacionar
     precisión con representación, unidades y redondeo, sin atribuir a más
     servidores una mejora automática de la calidad de una medición.
   - **Preguntas y práctica:** clasificar incidentes parecidos con consecuencias
     distintas; analizar qué significa que reservas esté disponible y responda
     correctamente durante una falla. Profundizar mecanismos en bloques posteriores.
   - **Fuentes:** [atributos de calidad](../wiki/topics/atributos-de-calidad.md);
     [OFF-013](../sources/extracted/OFF-013.md), pp. 15-19, 21, 27-28;
     [OFF-019](../sources/extracted/OFF-019.md), p. 22;
     [EXT-019](../sources/extracted/EXT-019.md), p. 1;
     [EXT-001](../sources/extracted/EXT-001.md), «Calidad»;
     complementos C03 y C16.

3. [pending] Calidad de diseño, del sistema y de la experiencia de uso
   - **Alcance:** integridad conceptual, mantenibilidad y modificabilidad,
     portabilidad, reusabilidad, soportabilidad, testeabilidad o verificabilidad,
     accesibilidad y usabilidad. Alcance y diferencias entre nombres empleados
     por las fuentes. Cambios, diagnósticos y tareas de usuarios como situaciones
     concretas para analizar estos atributos.
   - **Resultados:** distinguir accesibilidad de usabilidad y soportabilidad de
     administrabilidad; reconocer decisiones que facilitan cambios y pruebas;
     explicar beneficios y costos de abstraer, reutilizar o agregar configurabilidad.
   - **Preguntas y práctica:** comparar dos diseños frente a un cambio de
     proveedor y dos interfaces frente a una misma tarea. Identificar a quién
     beneficia cada mejora y cómo comprobarla.
   - **Fuentes:** [atributos de calidad](../wiki/topics/atributos-de-calidad.md);
     [OFF-013](../sources/extracted/OFF-013.md), pp. 17, 20-21, 27-28;
     [OFF-019](../sources/extracted/OFF-019.md), p. 22;
     [EXT-019](../sources/extracted/EXT-019.md), p. 1;
     [EXT-001](../sources/extracted/EXT-001.md), «Calidad»; complemento C15.

4. [pending] Escenarios medibles, prioridades y compromisos
   - **Alcance:** pasar de adjetivos generales a escenarios verificables;
     estímulo, origen, entorno, elemento afectado, respuesta y medida. Métrica,
     SLI, SLO y SLA; percentiles, ventanas de medición, carga y objetivos.
     Priorización de atributos, costo de satisfacerlos y conflictos entre ellos.
   - **Resultados:** formular escenarios completos de ejecución, cambio y uso;
     justificar una medida y su método de observación; detectar promedios o
     indicadores que ocultan problemas; expresar compromisos y supuestos.
   - **Preguntas y práctica:** especificar objetivos para reservar bajo carga,
     recuperarse de una falla y agregar un proveedor. Contrastar objetivos
     distintos para horarios y operaciones diferentes. Introducir un árbol de
     utilidad sencillo; retomar el método completo en el bloque 24.
   - **Fuentes:** [atributos](../wiki/topics/atributos-de-calidad.md),
     [árbol de utilidad](../wiki/topics/arbol-de-utilidad.md);
     [OFF-013](../sources/extracted/OFF-013.md), pp. 24, 28;
     [OFF-019](../sources/extracted/OFF-019.md), pp. 15, 17, 22, 26;
     [EXT-001](../sources/extracted/EXT-001.md), «Attribute Driven Design»;
     complementos C02 y C03.

5. [pending] Fundamentos de ejecución y recorrido de una solicitud
   - **Alcance:** proceso, hilo, memoria, disco, concurrencia, paralelismo y
     operaciones de entrada/salida. Cliente y servidor; IP, puertos, DNS,
     conexiones, HTTP y TLS. Ubicar latencia, recursos limitados, estado y
     posibles fallas en una interacción completa. Precisar la versión del
     protocolo cuando una explicación dependa de ella.
   - **Resultados:** seguir una solicitud desde el cliente hasta los datos y su
     respuesta; diferenciar ejecución local de comunicación remota; reconocer
     esperas, contención y fallas parciales sin suponer una red instantánea.
   - **Preguntas y práctica:** dibujar el recorrido de una reserva; localizar
     dónde se conserva su estado y qué sucede si falla cada participante.
   - **Fuentes:** [modelo 4+1](../wiki/topics/modelo-cuatro-mas-uno.md);
     [OFF-011](../sources/extracted/OFF-011.md), pp. 5-7, 9-13;
     [OFF-014](../sources/extracted/OFF-014.md), pp. 14-15;
     complemento C01. La mecánica de redes requiere este complemento.

6. [pending] Organización del software: módulos, capas y MVC
   - **Alcance:** responsabilidades, interfaces, dependencias y encapsulación;
     cohesión y acoplamiento como criterios de diseño. Estilo arquitectónico,
     patrón y tecnología. Capas lógicas, distribución física, monolito modular
     y MVC; separación de modelo, vista y controlador y sus colaboraciones.
   - **Resultados:** elegir límites a partir de responsabilidades y cambios;
     diferenciar separar código, procesos y despliegues; explicar los beneficios
     y costos de capas y MVC sin equipararlos con microservicios.
   - **Preguntas y práctica:** organizar reservas, pagos y notificaciones dentro
     de una aplicación; recorrer un cambio y evaluar qué dependencias afecta.
   - **Fuentes:** [estilos](../wiki/topics/estilos-arquitectonicos.md),
     [flujo de datos](../wiki/topics/flujo-de-datos.md),
     [MVC](../wiki/topics/modelo-vista-controlador.md);
     [OFF-014](../sources/extracted/OFF-014.md), pp. 24, 28-33, 48-51;
     [OFF-011](../sources/extracted/OFF-011.md), pp. 4-8, 13;
     [OFF-018](../sources/extracted/OFF-018.md), pp. 16-20;
     [EXT-001](../sources/extracted/EXT-001.md), «Estilos Arquitectónicos»
     y «Patrones a Nivel de Aplicación».

7. [pending] Representación y comunicación: 4+1, C4 y decisiones
   - **Alcance:** vistas y puntos de vista; módulos, componentes y conectores,
     asignación. Las cinco perspectivas de 4+1, niveles de C4, diagramas UML
     asociados, diagramas dinámicos y de despliegue. Audiencia, alcance y
     coherencia entre vistas. Registro breve de contexto, alternativas,
     decisión, consecuencias y motivos de revisión.
   - **Resultados:** elegir una representación según la pregunta; explicar
     correspondencias sin inventar un mapeo uno a uno; distinguir el contenedor
     de C4 del contenedor de ejecución; documentar la razón de una decisión.
   - **Preguntas y práctica:** representar el mismo caso mediante contexto,
     contenedores, una secuencia y despliegue; detectar contradicciones entre ellos.
   - **Fuentes:** [documentación](../wiki/topics/documentacion-de-arquitectura.md),
     [4+1](../wiki/topics/modelo-cuatro-mas-uno.md),
     [C4](../wiki/topics/modelo-c4.md);
     [OFF-011](../sources/extracted/OFF-011.md), pp. 2-15;
     [OFF-014](../sources/extracted/OFF-014.md), pp. 2-17, 23;
     [EXT-001](../sources/extracted/EXT-001.md), unidad 3; complemento C04.

8. [pending] APIs, contratos y modalidades de comunicación
   - **Alcance:** API como interfaz; protocolos y formatos; HTTP, recursos,
     métodos, errores, idempotencia y compatibilidad. Relación entre API HTTP,
     REST y RPC. Comunicación síncrona y asíncrona; polling, WebSocket y webhook;
     cliente web, aplicación móvil y recepción de notificaciones en el servidor.
   - **Resultados:** elegir una modalidad según latencia, participantes y
     conectividad; definir un contrato y su evolución; distinguir una conexión
     persistente de la persistencia de un dato y recepción de procesamiento.
   - **Preguntas y práctica:** comparar confirmar una reserva, consultar su
     estado y recibir una confirmación de pago. Analizar duplicados, desconexión
     y autenticación del emisor; retomar garantías en los bloques 17 y 21.
   - **Fuentes:** [integración](../wiki/topics/integracion-de-sistemas.md);
     [OFF-018](../sources/extracted/OFF-018.md), pp. 3, 5-9;
     [EXT-020](../sources/extracted/EXT-020.md), «Bucket de Soluciones»,
     entradas HTTP, Websockets y Webhooks; complementos C01 y C08.
     Ampliar el protocolo concreto al investigar el bloque.

9. [pending] Entrada y distribución del tráfico
   - **Alcance:** servidor web, proxy directo y reverso, balanceador, API
     gateway, BFF y CDN. Responsabilidades, recorrido y posible combinación;
     balanceo y health checks, terminación TLS, afinidad y estado de sesión;
     composición de respuestas, adaptación a clientes y límites de tráfico.
   - **Resultados:** ubicar cada función y justificarla con un requisito;
     distinguir repartir carga de adaptar una API; reconocer solapamientos y
     costos operativos; identificar qué componente todavía podría fallar.
   - **Preguntas y práctica:** incorporar web y móvil al caso; decidir si
     comparten API, necesitan BFF y cómo distribuir tráfico entre instancias.
     Diferenciar contenido estático de respuestas privadas o variables.
   - **Fuentes:** [patrones de comunicación](../wiki/topics/patrones-de-comunicacion-entre-servicios.md);
     [OFF-014](../sources/extracted/OFF-014.md), pp. 44-46;
     [OFF-018](../sources/extracted/OFF-018.md), p. 23;
     [EXT-001](../sources/extracted/EXT-001.md), «Patrones a Nivel de Comunicación»;
     [EXT-020](../sources/extracted/EXT-020.md), «Scalability»;
     complementos C01, C05 y C17. Profundizar CDN al investigar este bloque.

10. [pending] Seguridad: amenazas, identidad y límites de confianza
    - **Alcance:** confidencialidad, integridad, disponibilidad y amenazas;
      autenticación, autorización, sesiones, tokens, JWT, MFA y mínimo privilegio.
      TLS, cifrado en reposo y gestión de secretos; firewall de red, reglas de
      acceso, WAF, VPN y protección ante denegación de servicio. Límites de cada
      control y responsabilidades del cliente, aplicación e infraestructura.
    - **Resultados:** justificar un control contra una amenaza; localizar
      controles en el recorrido de una solicitud; diferenciar firma de cifrado
      y acceso a la red de permiso sobre un recurso. Evaluar usabilidad y costos.
    - **Preguntas y práctica:** proteger reservas públicas y administración;
      analizar acceso a una reserva ajena, consultas SQL inseguras y abuso de
      tráfico. Distinguir validación de entradas, consultas parametrizadas y
      controles de autorización.
    - **Fuentes:** [atributos](../wiki/topics/atributos-de-calidad.md);
      [OFF-013](../sources/extracted/OFF-013.md), pp. 17, 19, 28;
      [OFF-018](../sources/extracted/OFF-018.md), pp. 11, 23;
      [EXT-020](../sources/extracted/EXT-020.md), «Security» y entradas de seguridad;
      complementos C08, C09 y C18. Investigar identidad y VPN con documentación
      específica antes de enseñar sus flujos en detalle.

11. [pending] Persistencia: archivos, prevalencia, bases y ORM
    - **Alcance:** estado volátil y durable; serialización, archivos planos,
      estructurados, binarios e indexados. Recuperación mediante logs y
      snapshots en prevalencia; límites de memoria y concurrencia. Servicios
      de una base; base de objetos, modelo relacional y mapeo objeto-relacional.
    - **Resultados:** elegir un mecanismo acorde al acceso y recuperación;
      distinguir formato de archivo de garantías del almacenamiento; diferenciar
      una base de objetos de un ORM y explicar costos de transformación.
    - **Preguntas y práctica:** comparar configuración, exportaciones y reservas
      como datos con necesidades diferentes. Reconstruir el estado después de
      un reinicio e identificar qué escrituras deben haberse confirmado.
    - **Fuentes:** [persistencia](../wiki/topics/persistencia.md),
      [prevalencia](../wiki/topics/prevalencia.md),
      [bases relacionales](../wiki/topics/bases-de-datos-relacionales.md);
      [OFF-016](../sources/extracted/OFF-016.md), pp. 2-14, 23-24;
      [EXT-001](../sources/extracted/EXT-001.md), unidad 5 hasta «Bases de Datos».

12. [pending] Bases relacionales, transacciones y concurrencia
    - **Alcance:** entidades, relaciones, claves, restricciones, normalización,
      joins e índices. ACID, invariantes, transacciones, aislamiento, anomalías,
      bloqueos y control optimista; fallas de serialización y reintentos.
      Relacionar la forma de consultar con el costo de lectura y escritura.
    - **Resultados:** modelar reservas e impedir una doble confirmación bajo
      concurrencia; explicar qué garantiza el motor y qué depende del esquema,
      aislamiento y lógica de aplicación; justificar un índice y sus costos.
    - **Preguntas y práctica:** recorrer dos compras simultáneas del último
      cupo. Diseñar un experimento mínimo con una invariante verificable y
      comparar alternativas de control de concurrencia.
    - **Fuentes:** [bases relacionales](../wiki/topics/bases-de-datos-relacionales.md);
      [OFF-016](../sources/extracted/OFF-016.md), pp. 10, 13-14, 23;
      [EXT-001](../sources/extracted/EXT-001.md), «Bases de Datos»;
      complemento C07, §13.2. Profundizar índices y planes de consulta con la
      documentación del motor durante la investigación del bloque.

13. [pending] Modelos no relacionales y elección del almacenamiento
    - **Alcance:** documentos, clave-valor, familias de columnas, grafos y series
      temporales; distinguirlos del almacenamiento columnar analítico. Índices
      de búsqueda y búsqueda vectorial como necesidades específicas. Patrones
      de acceso, agregados, esquema, consultas, transacciones, volumen y operación.
    - **Resultados:** comparar modelos y motores concretos con los mismos
      requisitos; reconocer cuándo alcanza una base ya existente y cuándo
      justificar otra; verificar las garantías sin deducirlas de la etiqueta NoSQL.
    - **Preguntas y práctica:** elegir almacenamiento para cupos, catálogo,
      sesiones, telemetría y búsqueda; proponer una opción alternativa y señalar
      qué requisito decidiría entre ambas. Separar almacenamiento de archivos
      de la indexación de su contenido.
    - **Fuentes:** [bases no relacionales](../wiki/topics/bases-de-datos-no-relacionales.md);
      [OFF-016](../sources/extracted/OFF-016.md), pp. 14-25;
      [EXT-001](../sources/extracted/EXT-001.md), «Bases No Relacionales» y
      «Búsquedas»; complementos C06 y C07. Grafos, series temporales y las
      diferencias internas de modelos requieren el complemento C06.

14. [pending] Caché, frescura e invalidación
    - **Alcance:** caché local y compartida, claves, hit y miss, TTL y expulsión;
      cache-aside y comparación con otras políticas de lectura y escritura.
      Datos obsoletos, invalidación concurrente, arranque en frío y avalanchas
      de solicitudes. Diferenciar caché, réplica y almacenamiento autoritativo.
    - **Resultados:** justificar qué cachear y por cuánto tiempo; diseñar la
      actualización y recuperación ante falla; estimar el beneficio según
      patrón de acceso y medir tanto latencia como frescura.
    - **Preguntas y práctica:** comparar cachear un catálogo con cachear cupos
      disponibles; analizar una lectura concurrente con una actualización y
      qué sucede al perder toda la caché.
    - **Fuentes:** [EXT-001](../sources/extracted/EXT-001.md), «Tweets» y «Timeline»;
      [EXT-020](../sources/extracted/EXT-020.md), «Bucket de Soluciones» y
      «Performance»; complemento C10, especialmente «Problems and considerations».

15. [pending] Replicación, particionamiento y consistencia distribuida
    - **Alcance:** escalamiento vertical y horizontal; réplicas, primario-secundario,
      múltiples escritores, sincronización, failover y retraso de replicación.
      Sharding, claves de partición, localidad, hotspots y consultas entre shards.
      Consistencia entre réplicas, lectura de las propias escrituras y CAP.
    - **Resultados:** distinguir escalar lecturas de escrituras; elegir una
      partición a partir de consultas; razonar una partición de red y explicar
      el compromiso de CAP con sus supuestos. Separar consistencia de ACID,
      consistencia entre réplicas y disponibilidad medida por un SLO.
    - **Preguntas y práctica:** contrastar particionar por evento, usuario o
      fecha; reconstruir un caso con escritura confirmada y lectura retrasada;
      explicar el argumento de indistinguibilidad de CAP y sus límites prácticos.
    - **Fuentes:** [escalamiento](../wiki/topics/escalamiento-de-datos.md);
      [EXT-001](../sources/extracted/EXT-001.md), «Escalamiento de Bases Relacionales»,
      «Alternativas de Bases Relacionales» y unidad 6, como caso histórico;
      complementos C06, C07 y C11, §2 y §4.

16. [pending] Procesamiento de datos, analítica y eventos
    - **Alcance:** OLTP y OLAP, reporting, data warehouse, ETL y costo de
      agregaciones. Batch secuencial, pipes and filters y flujo continuo.
      Productores, canales y consumidores; procesamiento individual, de
      streams, complejo y online según la clasificación del curso.
    - **Resultados:** elegir un flujo según volumen, latencia y recuperación;
      justificar separar cargas operativas y analíticas; distinguir evento,
      comando y dato de una medición, y especificar ventanas y frescura.
    - **Preguntas y práctica:** generar reportes de reservas y detectar patrones
      de sensores; evaluar fallas de etapas, reprocesamiento y datos tardíos.
      Retomar precisión, throughput y tiempo de respuesta de punta a punta.
    - **Fuentes:** [flujo de datos](../wiki/topics/flujo-de-datos.md),
      [eventos](../wiki/topics/procesamiento-de-eventos.md),
      [bases relacionales y analíticas](../wiki/topics/bases-de-datos-relacionales.md);
      [OFF-014](../sources/extracted/OFF-014.md), pp. 25-33, 52-56;
      [OFF-016](../sources/extracted/OFF-016.md), pp. 11, 23-25;
      [OFF-017](../sources/extracted/OFF-017.md), p. 7; complemento C06.

17. [pending] Mensajería, colas, publicación-suscripción y garantías
    - **Alcance:** broker, pub-sub, forwarder-receiver y client-dispatcher-server
      del curso; colas de trabajo, consumidores competidores, tópicos y logs de
      eventos. Persistencia, confirmaciones, reentrega, orden, retención,
      particiones, consumidores idempotentes, deduplicación y dead-letter queue.
      Alcance de at-most-once, at-least-once y exactly-once.
    - **Resultados:** elegir un modelo por el destino del mensaje y la necesidad
      de replay; distinguir entrega de procesamiento y efectos externos;
      especificar garantías y sus costos sin asumirlas por el nombre del patrón.
    - **Preguntas y práctica:** decidir cómo distribuir notificaciones y trabajo
      de reportes; recorrer una falla después de procesar y antes de confirmar.
      Analizar acumulación de trabajo y qué ocurre con un consumidor nuevo.
    - **Fuentes:** [comunicación distribuida](../wiki/topics/comunicacion-distribuida.md);
      [OFF-014](../sources/extracted/OFF-014.md), pp. 34-47;
      [EXT-001](../sources/extracted/EXT-001.md), «Estilos Arquitectónicos»;
      [EXT-020](../sources/extracted/EXT-020.md), entrada «Queues»;
      complemento C12, patrones y sección de garantías de Kafka.

18. [pending] Integración, SOA y procesos de negocio
    - **Alcance:** integración punto a punto, adapters, middleware, hub y ESB;
      contratos y granularidad de servicios, registro y descubrimiento.
      SOA, composición, orquestación y coreografía; BPM y BAM; gobierno de
      versiones, políticas, propiedad y monitoreo.
    - **Resultados:** identificar acoplamientos de una integración; justificar
      intermediación y composición; separar decisiones de negocio de transporte;
      evaluar los beneficios y costos de centralizar responsabilidades.
    - **Preguntas y práctica:** integrar reservas con un proveedor heredado,
      pagos y contabilidad; definir contratos, responsables y evolución.
    - **Fuentes:** [integración](../wiki/topics/integracion-de-sistemas.md),
      [SOA](../wiki/topics/arquitectura-orientada-a-servicios.md);
      [OFF-018](../sources/extracted/OFF-018.md), pp. 2-12;
      [EXT-001](../sources/extracted/EXT-001.md), «SOA» y «Servicios».

19. [pending] Monolitos y microservicios: límites técnicos y organizacionales
    - **Alcance:** artefacto de despliegue, modularidad, autonomía de equipos y
      capacidades del negocio. Descomposición por subdominios, propiedad de
      datos, dependencias entre servicios, madurez operativa y DevOps.
      Costos de distribución y condiciones para conservar o extraer módulos.
    - **Resultados:** comparar una aplicación modular y servicios desplegables
      por separado; elegir límites por requisitos y cambios; explicar por qué
      escalar o sumar equipo no determina por sí solo una descomposición.
    - **Preguntas y práctica:** evaluar dos organizaciones con el mismo producto
      y equipos diferentes. Diseñar una extracción y reconocer si requiere
      tantos despliegues coordinados que se pierde la independencia buscada.
    - **Fuentes:** [microservicios](../wiki/topics/microservicios.md);
      [OFF-018](../sources/extracted/OFF-018.md), pp. 14-22, 25;
      [EXT-001](../sources/extracted/EXT-001.md), «Microservicios» y
      «Patrones a Nivel de Aplicación».

20. [pending] Datos entre servicios: 2PC, sagas, CQRS y event sourcing
    - **Alcance:** propiedad e invariantes, transacción local y distribuida,
      coordinación en dos fases, bloqueo y recuperación. Sagas orquestadas o
      coreografiadas, compensaciones e irreversibilidad. Agregados, modelos de
      lectura y escritura, proyecciones y event sourcing como registro autoritativo.
      Reconstrucción, versionado y problema de actualizar datos y publicar eventos.
    - **Resultados:** elegir una estrategia de coordinación; explicar estados
      intermedios y fallas de compensación; distinguir CQRS de réplicas y de
      event sourcing. Reconocer cuándo la complejidad excede el beneficio.
    - **Preguntas y práctica:** coordinar reserva, cobro y devolución; reconstruir
      una proyección duplicada o atrasada. Investigar outbox como complemento
      para la publicación de eventos antes de proponer una implementación.
    - **Fuentes:** [patrones de datos](../wiki/topics/patrones-de-datos-distribuidos.md);
      [OFF-018](../sources/extracted/OFF-018.md), p. 21;
      [EXT-001](../sources/extracted/EXT-001.md), «Patrones a Nivel de Aplicación»;
      complemento C13. La mecánica completa de 2PC y outbox requiere investigación
      primaria adicional al enseñar este bloque.

21. [pending] Resiliencia y control de la sobrecarga
    - **Alcance:** fallas parciales, timeouts y deadlines; reintentos limitados,
      backoff y jitter; idempotencia y resultado incierto de una operación.
      Circuit breaker, aislamiento de recursos, backpressure, límites de
      concurrencia, degradación y propagación de fallas.
    - **Resultados:** diseñar una política coherente de tiempos y reintentos;
      distinguir un servicio caído de uno lento o saturado; explicar cómo una
      medida puede empeorar otra falla y cómo observar sus efectos.
    - **Preguntas y práctica:** simular mentalmente un pago confirmado cuya
      respuesta se pierde; calcular amplificación por reintentos encadenados;
      elegir qué funcionalidad degradar y cuándo cortar llamadas.
    - **Fuentes:** [patrones de comunicación](../wiki/topics/patrones-de-comunicacion-entre-servicios.md);
      [EXT-001](../sources/extracted/EXT-001.md), «Patrones a Nivel de Comunicación»;
      complemento C14, «Timeouts», «Retries and backoff» y «Jitter»;
      C12 para presión de consumidores y C03 para observación.

22. [pending] Despliegue y ejecución: infraestructura y abstracciones
    - **Alcance:** on-premise y cloud, responsabilidades operativas, regiones y
      dominios de falla; máquinas físicas, virtuales, contenedores y serverless.
      Imágenes, procesos, configuración, secretos y volúmenes; Kubernetes,
      nodos, pods, servicios, estado deseado, health checks y escalamiento.
      Sidecars y service mesh, costos y dependencia del proveedor.
    - **Resultados:** ubicar qué administra cada parte; distinguir aislamiento,
      empaquetado, programación y escalamiento; elegir una alternativa compatible
      con carga, estado y equipo; reconocer el costo de operar una plataforma.
    - **Preguntas y práctica:** desplegar conceptualmente la misma aplicación
      con alternativas distintas y explicar recuperación, datos y actualización.
      Contrastar un job esporádico con un proceso que conserva conexiones.
    - **Fuentes:** [infraestructura](../wiki/topics/infraestructura-de-despliegue.md);
      [OFF-018](../sources/extracted/OFF-018.md), p. 24;
      [EXT-001](../sources/extracted/EXT-001.md), «Patrones a Nivel de Infraestructura»;
      [EXT-020](../sources/extracted/EXT-020.md), entrada «Hosting»;
      complemento C19. Profundizar serverless y service mesh con documentación
      del producto elegido durante el bloque.

23. [pending] Operación, observabilidad y recuperación
    - **Alcance:** métricas, logs, trazas, correlación, alertas y experiencia de
      usuario; SLI y SLO en producción, presupuesto de errores y capacidad.
      Redundancia, backups, restauración, recuperación ante desastres y objetivos
      de tiempo y pérdida de datos. Despliegues progresivos, rollback, migraciones
      compatibles, costo de infraestructura y trabajo operativo.
    - **Resultados:** seleccionar señales accionables; relacionar diagnóstico
      con soportabilidad y auditabilidad; distinguir replicar de poder restaurar;
      proponer comprobaciones de recuperación y de una actualización segura.
    - **Preguntas y práctica:** investigar una reserva lenta siguiendo sus
      dependencias; analizar borrado accidental y despliegue defectuoso; definir
      evidencia de recuperación y un objetivo explícito de frescura de backups.
    - **Fuentes:** [evaluación](../wiki/topics/evaluacion-de-arquitecturas.md),
      [gobierno](../wiki/topics/gobierno-de-arquitectura.md);
      [OFF-019](../sources/extracted/OFF-019.md), pp. 17, 22;
      [OFF-018](../sources/extracted/OFF-018.md), pp. 11, 14, 25;
      [EXT-001](../sources/extracted/EXT-001.md), «Platform Engineering»;
      C03. Recuperación y estrategias de despliegue requieren investigación
      primaria adicional: las fuentes del curso sólo aportan cobertura parcial.

24. [pending] Diseño y evaluación: ADD, árbol de utilidad y ATAM
    - **Alcance:** transformación de drivers en arquitectura candidata;
      adaptación docente de ADD y contraste con la evaluación. Escenarios,
      checklists, métricas, prototipos, simulaciones y modelos. Árbol de utilidad,
      prioridad y dificultad; fases, participantes y resultados de ATAM y su
      versión liviana. Riesgos, no riesgos, sensibilidad y compromisos.
    - **Resultados:** conducir un diseño y una evaluación acotados; distinguir
      razonamiento cualitativo de medición; justificar técnica y esfuerzo.
      Explicar modelos sencillos de latencia y disponibilidad con supuestos
      explícitos de dependencia, independencia y fallas correlacionadas.
    - **Preguntas y práctica:** evaluar dos arquitecturas de reservas contra los
      mismos escenarios, incluido un cambio y una falla común. Contrastar con
      el caso docente CAAS y defender riesgos asumidos y pruebas pendientes.
    - **Fuentes:** [ADD](../wiki/topics/diseno-dirigido-por-atributos.md),
      [evaluación](../wiki/topics/evaluacion-de-arquitecturas.md),
      [ATAM](../wiki/topics/atam.md), [árbol](../wiki/topics/arbol-de-utilidad.md);
      [OFF-013](../sources/extracted/OFF-013.md), pp. 16, 24, 28;
      [OFF-019](../sources/extracted/OFF-019.md), pp. 12-32;
      [OFF-015](../sources/extracted/OFF-015.md), pp. 6-10, 15-24, 30-41;
      [EXT-001](../sources/extracted/EXT-001.md), «Attribute Driven Design» y
      «Validación de Proyectos Legacy o Third-Party»; C02 y C20.

25. [pending] Evolución, gobierno e incertidumbre
    - **Alcance:** anticipación y adaptación, BDUF, YAGNI, arquitectura
      intencional, emergente y runway. Decisiones reversibles, costo de migrar,
      compatibilidad y revisión de supuestos. Guardrails y plataformas internas.
      Residualidad con el alcance documentado por los apuntes: estresores,
      residuos y preguntas sobre fallas conjuntas.
    - **Resultados:** proponer una evolución incremental y sus señales de
      revisión; balancear autonomía con coherencia; reconocer afirmaciones que
      necesitan evidencia adicional antes de aplicar un método.
    - **Preguntas y práctica:** cambiar escala, proveedor y organización del
      caso; identificar el próximo paso justificado y lo que necesita medirse.
      Contrastar análisis de escenarios y estresores sin adjudicar limitaciones
      universales a ADD ni inventar un cálculo de residual index.
    - **Fuentes:** [evolución](../wiki/topics/evolucion-de-la-arquitectura.md),
      [gobierno](../wiki/topics/gobierno-de-arquitectura.md),
      [residualidad](../wiki/topics/teoria-de-la-residualidad.md);
      [OFF-019](../sources/extracted/OFF-019.md), pp. 3-11, 32;
      [OFF-018](../sources/extracted/OFF-018.md), pp. 11-12;
      [EXT-001](../sources/extracted/EXT-001.md), unidad 4 y
      «Residuality Theory (Video)». Ver la brecha de fuentes indicada abajo.

26. [pending] Integración, transferencia y preparación de examen
    - **Alcance:** diseñar y comparar soluciones completas con requisitos,
      restricciones, vistas, recorridos, selección de herramientas, riesgos y
      alternativas. Cambiar de dominio, carga y organización. Integrar el
      vocabulario y las familias de temas del repaso oficial.
    - **Resultados:** defender cada pieza por un mecanismo y un escenario;
      proponer una arquitectura mínima suficiente y explicar cómo evoluciona;
      adaptar el razonamiento a un caso nuevo y reconocer información faltante.
      Explicar los conceptos del examen con precisión y ejemplos propios.
    - **Preguntas y práctica:** resolver casos inventados de reservas,
      telemetría y aplicación interna; retirar un componente y analizar el
      efecto. Revisar una propuesta con errores y explicitar qué evidencia
      haría cambiar la decisión. Discutir preguntas transversales antes de
      considerar completo el recorrido.
    - **Fuentes:** [índice de la wiki](../wiki/index.md) y las fuentes de los
      bloques anteriores; [OFF-017](../sources/extracted/OFF-017.md), pp. 2-11.
      Las prácticas catalogadas pueden usarse como contexto opcional;
      resolverlas requiere su flujo específico de planificación y ejecución.

## Fuentes complementarias consultadas

Estas referencias amplían la cobertura práctica. Los códigos C01-C20 son
referencias internas de este mapa, no entradas nuevas del catálogo. Fueron
consultadas el 16 de octubre de 2026; sus ejemplos y capacidades no se atribuyen
a la cátedra. Al investigar cada bloque, verificar versiones y seguir las
secciones específicas y referencias primarias pertinentes.

- **C01, redes y HTTP:** MDN, [How the web works](https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Web_standards/How_the_web_works),
  secciones sobre participantes y DNS; [Overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Overview),
  componentes, mensajes, conexiones y estado.
- **C02, escenarios de calidad:** SEI, [Eliciting and Specifying Quality Attribute Requirements](https://sei.cmu.edu/documents/5465/2013_018_101_60984.pdf),
  formulación en seis partes; [Reasoning About Software Quality Attributes](https://www.sei.cmu.edu/library/reasoning-about-software-quality-attributes/),
  escenarios generales y razonamiento sobre atributos.
- **C03, objetivos y operación:** Google SRE, [Service Level Objectives](https://sre.google/sre-book/service-level-objectives/),
  terminología, agregación, indicadores y objetivos;
  [Monitoring Distributed Systems](https://sre.google/sre-book/monitoring-distributed-systems/),
  señales, síntomas y alertas.
- **C04, C4:** sitio del modelo, [Diagrams](https://c4model.com/diagrams),
  estructura estática, diagramas de apoyo y selección de niveles.
- **C05, adaptación a clientes:** Microsoft, [Backends for Frontends](https://learn.microsoft.com/en-us/azure/architecture/patterns/backends-for-frontends),
  contexto, costos y condiciones de aplicación.
- **C06, modelos de datos:** Microsoft, [Understand data models](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/understand-data-store-models),
  características por modelo y heurísticas de selección y combinación.
- **C07, garantías concretas de motores:** PostgreSQL,
  [Transaction Isolation](https://www.postgresql.org/docs/18/transaction-iso.html),
  §13.2, anomalías y niveles de aislamiento; MongoDB,
  [Transactions](https://www.mongodb.com/docs/manual/core/transactions/),
  soporte, alcance y costos de transacciones.
- **C08, seguridad de aplicaciones:** OWASP,
  [REST Security Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/REST_Security_Cheat_Sheet.html),
  HTTPS, control de acceso, JWT, validación y auditoría;
  [SQL Injection Prevention](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html),
  defensas primarias y consultas parametrizadas.
- **C09, WAF y DDoS:** AWS,
  [What are AWS WAF and AWS Shield?](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html),
  alcance de inspección HTTP/HTTPS y protección en distintas capas.
- **C10, caché:** Microsoft, [Cache-Aside](https://learn.microsoft.com/en-us/azure/architecture/patterns/cache-aside),
  flujo de lectura, invalidación, consistencia y condiciones de aplicación.
- **C11, límites de distribución:** Seth Gilbert y Nancy Lynch,
  [Perspectives on the CAP Theorem](https://groups.csail.mit.edu/tds/papers/Gilbert/Brewer2.pdf),
  §2, definiciones y argumento de imposibilidad; §4, consecuencias prácticas.
- **C12, mensajería:** Microsoft,
  [Competing Consumers](https://learn.microsoft.com/en-us/azure/architecture/patterns/competing-consumers)
  y [Publisher-Subscriber](https://learn.microsoft.com/en-us/azure/architecture/patterns/publisher-subscriber),
  distribución del trabajo, duplicados, orden y errores;
  Apache Kafka, [Design](https://kafka.apache.org/41/design/design/),
  sección de garantías de entrega y límites de procesamiento exactamente una vez.
- **C13, datos y patrones:** Microsoft,
  [CQRS](https://learn.microsoft.com/en-us/azure/architecture/patterns/cqrs),
  modelos con almacenamiento compartido o separado;
  [Event Sourcing](https://learn.microsoft.com/en-us/azure/architecture/patterns/event-sourcing),
  registro autoritativo, reconstrucción y complejidad;
  [Saga](https://learn.microsoft.com/en-us/azure/architecture/patterns/saga),
  coordinación, transacciones compensatorias y fallas.
- **C14, resiliencia:** Amazon Builders' Library,
  [Timeouts, retries, and backoff with jitter](https://aws.amazon.com/builders-library/timeouts-retries-and-backoff-with-jitter/),
  selección de tiempos, efectos laterales y amplificación de carga.
- **C15, accesibilidad:** W3C WAI,
  [Introduction to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/),
  alcance, necesidades y ejemplos de barreras.
- **C16, precisión:** documentación de Python,
  [Floating-Point Arithmetic: Issues and Limitations](https://docs.python.org/3/tutorial/floatingpoint.html),
  error de representación y límites de redondear la presentación.
- **C17, balanceo:** NGINX,
  [Using nginx as HTTP load balancer](https://nginx.org/en/docs/http/load_balancing.html),
  métodos de distribución, persistencia de sesión y comprobaciones de salud.
- **C18, red:** AWS VPC,
  [Control traffic using security groups](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-security-groups.html),
  reglas de entrada/salida y alcance sobre recursos.
- **C19, ejecución:** Docker,
  [What is Docker?](https://docs.docker.com/get-started/docker-overview/),
  arquitectura, imágenes y contenedores; Kubernetes,
  [Overview](https://kubernetes.io/docs/concepts/overview/),
  capacidades, límites y estado deseado.
- **C20, evaluación:** SEI,
  [Architecture Tradeoff Analysis Method Collection](https://www.sei.cmu.edu/library/architecture-tradeoff-analysis-method-collection/),
  objetivos de calidad, escenarios, riesgos y compromisos.

## Cobertura del material del curso

Se revisaron todos los temas de arquitectura del índice de la wiki, el catálogo,
los extractos OFF-011 y OFF-013 a OFF-019, EXT-019, EXT-020 y las unidades 1 a 7
de EXT-001. Se inspeccionaron en los originales las tablas de atributos, drivers,
diagramas de estilos y MVC, persistencia y prevalencia, patrones de integración,
despliegue, árbol de utilidad y el caso docente CAAS cuando la extracción no
conservaba su contenido visual. Las páginas citadas son posiciones en el PDF;
las referencias a los apuntes usan sus títulos de sección.

| Tema del repaso OFF-017 | Bloques del recorrido |
| --- | --- |
| Arquitectura, requisitos y atributos de calidad | 1-4; retomados en 9-25 |
| Vistas 4+1 y diagramas | 7; aplicados en 24 y 26 |
| Dataflow y sistemas interactivos | 6 y 16 |
| Comunicación distribuida y eventos | 8, 16-17 |
| Evaluación y ATAM | 4 y 24 |
| Persistencia | 11-16 |
| Integración, SOA y gateway | 8-9, 18-20 |

## Desacuerdos, límites y tareas de investigación por bloque

- **Garantías de bases:** OFF-016, p. 14, admite variantes NoSQL con o sin
  ACID; las recomendaciones resumidas de sus pp. 24-25 y las etiquetas de
  EXT-020 son más amplias que una especificación de motor. En los bloques 12,
  13 y 15 se contrastarán con C07, indicando motor, configuración y operación.
  La descripción introductoria del aislamiento se precisará con sus niveles.
- **Columnas:** OFF-016 y EXT-001 reúnen bajo esa palabra ejemplos y
  propiedades de almacenamiento columnar y familias de columnas. El bloque 13
  incorporará la distinción con C06, conservando la atribución docente.
- **Prevalencia y ORM:** EXT-001 y EXT-020 describen un snapshot por cambio;
  OFF-016, pp. 7-8, distingue log y snapshots. El bloque 11 expondrá ambas
  formulaciones y el mecanismo del original. También distinguirá base de objetos
  de ORM; no son nombres intercambiables.
- **CAP:** EXT-001 y EXT-020 ofrecen reglas abreviadas y clasificaciones de
  motores. El bloque 15 usará las definiciones y el escenario de C11 para
  delimitar el argumento; no derivará una arquitectura sólo de tres letras.
- **CQRS y event sourcing:** EXT-001 se concentra en bases de lectura
  separadas y suscripciones a eventos. C13 permite estudiar variantes de CQRS
  y precisar el papel autoritativo del historial en event sourcing. La cobertura
  de 2PC y publicación mediante outbox sigue siendo parcial: debe ampliarse
  antes de enseñar los detalles del bloque 20.
- **Mensajería:** las observaciones de EXT-001 sobre recepción retroactiva y
  caída del broker describen su esquema. El bloque 17 verificará retención,
  durabilidad, redundancia y orden del mecanismo concreto. Exactly-once requiere
  explicitar la frontera de la garantía, incluidos los efectos externos (C12).
- **Seguridad:** EXT-020 contiene atajos como validar en la SPA para SQL
  injection y asociaciones generales entre WAF y DDoS. El bloque 10 los
  contrastará con consultas parametrizadas, controles de servidor y el alcance
  de protección por capa de C08-C09. El cifrado en reposo se analizará junto con
  controles de acceso y claves, sin tratarlo como solución a cualquier intrusión.
- **Calidad y medición:** las definiciones de confiabilidad y el alcance de
  algunos nombres varían entre OFF-013, OFF-019 y los apuntes; comparar su uso
  con ejemplos. Para SLI/SLO/SLA, exponer la diferencia entre OFF-019, p. 17,
  y «Validación de Proyectos Legacy o Third-Party» de EXT-001, con apoyo de C03.
- **Modelos y casos históricos:** los ejemplos de disponibilidad de OFF-015,
  p. 31, necesitan supuestos de independencia y conmutación; las latencias de
  p. 32 presentan unidades distintas entre texto y figura. El bloque 24 deberá
  explicitarlas y recalcular ejemplos consistentes. El caso Twitter se usará
  por sus patrones de acceso y su contexto histórico, sin afirmar que describe
  el sistema actual ni universalizar sus estimaciones y restricciones.
- **Ampliaciones profesionales:** redes, identidad, recuperación, despliegues,
  service mesh y protocolos concretos tienen cobertura desigual en el curso.
  Los complementos identifican puntos de partida; study-block debe completar
  la investigación específica de los bloques 5, 8-10, 12, 20, 22 y 23 antes de
  enseñar sus detalles. No se promete cobertura de implementación no investigada.
- **Residualidad:** sólo hay un resumen externo de un video sin una referencia
  primaria suficiente para desarrollar el método completo ni calcular residual
  index. El bloque 25 puede analizar ese resumen y su límite. Una profundización
  formal requiere localizar y verificar fuentes primarias antes de ampliar el mapa.

## Continuación

Comenzar con study-block en el bloque 1. El estado inicial indica el próximo
bloque a trabajar; no implica que ya se haya impartido o evaluado. Tras el
último bloque, discutir las preguntas de integración antes de marcar el
recorrido completo.
