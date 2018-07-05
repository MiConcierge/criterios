# Criterios de Calidad

> Esta es una guia general

Como en cualquier flujo de trabajo, todas y cada una de las partes involucradas en los diferentes procesos son fundamentales y, por ende, la falla de alguna de ellas tiene un impacto directo en el resto.
Para evitar inconvenientes y malos entendidos decidimos crear esta suerte de guía rápida que enumera recomendaciones, consejos, sugerencias y algún que otro pedido puntual, esperando optimizar un curso de acción que debería funcionar de manera aceitada asegurando eficiencia en el desempeño y buenos resultados.
No obstante, no es la intención de esta guía delimitar formas de actuar, ni tampoco moldear comportamientos.
Queremos que quede claro que podés trabajar de la manera que te resulte más práctica y útil. Nos interesa que te sientas cómodo porque eres una parte importante de nuestro equipo de trabajo y sabemos que tu aporte es sumamente valioso.
Sin embargo, sea cual sea la forma en que elijas desempeñar tus actividades, vamos a necesitar que no pases por alto ciertas pautas.
Simplemente con eso, nos estarás ayudando de manera significativa a mantener (e inclusive hacer crecer) el prestigio con esfuerzo ya consolidado.


## Desarrollo de interfaz

Como desarrollador, tu principal responsabilidad es la de implementar la interfaz final sobre la cual van a interactuar los usuarios. Esto no es simplemente traducir un Estilo a la technologia, sino que es pulir la interacción con el usuario y establecer los criterios necesarios para que la UX sea lo mejor posible, creando todo desde las adaptaciones responsive hasta esos pequeños detalles (como animaciones sutiles y una excelente performance) que hacen que una interfaz pase de muy buena a excelente.

Para esto tomamos en cuenta nuestro punto de partida, que es la etapa de wireframing y diseño. En lo posible, es conveniente que te involucres temprano en el proyecto para asegurarte de que el diseño de UI/UX puede ser llevado a cabo correctamente, al igual que poder cechar el costado técnico del proyecto para marcar las cosas que hay que tener en cuenta antes de comenzar con la implementación.

### Check list de implementacion
  - ¿Cuál es el target de browsers y dispositivos? Verificá esto con las especificaciones del trabajo.
  - ¿Cómo son los :hover, :active y animaciones del site? Trabajá con los diseñadores para llegar al mejor resultado posible.
  - ¿Hay componentes que tengan un funcionamiento particular? (Headers fixed, fondos con parallax, transiciones de elementos).
  - ¿Cuánta libertad hay para modificar el diseño? Esto es importante en sitios donde se espera una representación pixel-perfect del diseño, por más complejo que sea. Si este es el caso, y   hay que hacer un cambio, asegurate de comunicarlo para que no haya malentendidos.
  - ¿Qué se hara con esta implementación? ¿Es conveniente crear una estructura que después permita adaptarla a otra app/plataforma?
  - ¿Esto va sobre un framework de server o sólo hay que entregar el `static`? Es conveniente en lo posible trabajar sobre la implementación final, ya que aceleramos el trabajo de integración.
  - ¿Hay algún requerimiento en lo que refiere a tecnologías? Por ejemplo, usar Angular, alguna versión de jQuery en particular, evitar elementos de HTML5, entre otras. Documentalas apropiadamente para que se conozcan las restricciones del proyecto.
  - ¿Cómo va a ser la integración final con el producto? ¿Quién se encarga de los merges y subida a producción?
  - ¿Hay algún estándar de código que haya que seguir?
  - ¿Cómo hacemos para avisar que un entregable está listo? Establecé apenas empiece el proyecto una metodología para avisar (issues, trello, tickets) para saber qué cosas se pueden dar por hechas. Recuerda siempre la revisión final antes de confirmar un entregable.

### Nuestras reglas principales

#### PROLIJIDAD ANTE TODO
Nuestras guidelines son muy simples: Usamos UTF-8 para todo, tabulado con 2 espacios. Trabajamos en inglés a menos que haya una excepción para el proyecto (como este manual :P).

Tratá de que el código sea claro y modular. Como regla general no te repitas, y asume que quien va a trabajar contigo en el proyecto es un asesino serial que sabe dónde vives.

####  SHOW AND TELL
Usamos Pull Requests para hacer una revisión de código antes de dar por finalizada una feature. De esta forma damos lugar a que nuestros compañeros de equipo puedan asegurar que se están cumpliendo nuestros estándares de calidad, al igual que nos otorga un segundo punto de vista para detectar problemas con el código.

Asimismo, en features complejas es conveniente que todos se sumen para testear y dar insights valiosos, los cuales pueden discutirse y corregirse antes de terminar cada objetivo.

####  TEST, TEST, TEST
Chrome no es el único browser que existe. Desde el costado visual, nuestros estándares de compatibilidad son muy simples y sólo lleva unos minutos verificar que el funcionamiento de una interfaz es apto para la mayoría de los usuarios. A medida que aumenta la complejidad del proyecto, es recomendable incorporar unit tests y visual regression tests. Los tests no son tanto para ver si lo que acabás de terminar está bien. Es para enterarte si lo rompiste después.

Testeá siempre antes de enviar un entregable.

En desktop, como política general soportamos los browsers principales (Chrome, Firefox, Edge, Safari). Asimismo, todos nuestros sites son responsive con soporte mobile por defecto.

En mobile, dada la mayor variación y disponibilidad de hardware, tomamos como base los dispositivos de referencia de iOS y Android, que son los iPhone y Pixel/Nexus disponibles comercialmente durante los últimos 12 meses, incluyendo sus sistemas operativos.

Estos estándares son una guía general y deben evaluarse por proyecto para garantizar un excelente resultado final. Analizá las características del sitio en la etapa de análisis para no tomar una decisión dogmática -y seguramente incorrecta-. Recordá que no podemos ofrecer una excelente UX si la mayoría de usuarios no puede usar el sitio/app.

Además de esto, van las consideraciones que tomamos para todo proyecto.

#### USÁ GIT FLOW
Git Flow es una metodología que nos permite trabajar con mayor comodidad en un repositorio. Dale una leída al documento, pero lo que tenés que saber es lo siguiente: Usá siempre branches para nuevas features y fixes (feature-redesign), los cuales se mergean a dev para testearlos y recién una vez testeados los mandamos a master.

Desplegamos una nueva version cada Jueves despues de la hora de la comida (o cuando todos hayan comido).
El flujo para el deployment, se llevara a cabo ejecutando todas las pruebas necesesarias del proyecto, una vez que todas hayan sucedido, genera los pull request correspondientes para hacer una code review y finalmente terminar en distribucion.

#### COMENTÁ LAS COSAS "RARAS"
Uno siempre termina usando un hack para resolver alguna issue de compatibilidad, o bien termina implementando una feature compleja de corrido sin escribir un sólo comment. Dejá un comentario explicando brevemente la solución o el porqué de la misma para evitar traumas futuros. Si no lo hacés, seguramente te des cuenta de que el código que escribiste es confuso en el momento de la code review.

#### PEDÍ LA OPINIÓN DE OTRO DEV
A uno siempre se le escapan cosas o termina haciendo cosas por impulso. Siempre está bueno consultar con otra persona cada tanto para que le pegue un vistazo al trabajo a medida que va avanzando. Es algo que sólo lleva unos minutos y eleva notablemente la calidad del trabajo final, ya que terminás tomando experiencia prestada de alguien que por ahí ya se topó con el mismo problema antes.

## Diseño e Ideas

### Etapas de diseño
> UX -> UI -> UI Kit

### Mejor UX

La etapa de UX trabaja sobre la experiencia general del usuario asociada al uso del producto a crear. Los wireframes adquieren especial protagonismo en esta fase, no solo porque permiten delinear la estructura de las diferentes secciones del sitio o app (teniendo en cuenta arquitectura de la información, usabilidad, flow de navegación, etc.), sino porque, además, es a través de ellos que se definen las posibilidades de interacción.

### Mejores Ideas

Esta etapa suele ser la más larga de todo el proceso de diseño. ¡No desesperes! Es importante ser muy metódico y prolijo en la organización de archivos, principalmente cuando los proyectos adquieren grandes dimensiones. Pero más importante es considerar en cada una de tus decisiones cumple con los requerimientos del feature; no desde un rol de sumisión, sino más bien proactivo.

No obstante, nunca dejés de dar tu opinión si hay algo que piensas que podría hacerse de otra manera más efectiva. Sé cauteloso respecto a la forma en que redactás tus enunciados y cuidá la ortografía. Frases como "entiendo tu punto, pero opino que…" o "me parece bien lo que dices, pero considero…" son una buena forma de dar a conocer tu postura sin sonar pedante. No busques imponer tus ideas sino sugerir o proponer cambios con argumentos. Si no estás seguro de lo que escribiste, pedile a alguien más que lo lea y te dé su opinión.

> nunca dejés de dar tu opinión si hay algo que pensás podría hacerse de otra manera más efectiva.

### Mejor UI

Una vez que los wireframes pasaron por, al menos, 2 iteraciones y fueron aprobados, se procede al desarrollo de UI, en el cual se define el Look and Feel que tendrá el sitio/app (enfoque conceptual y lenguaje gráfico a utilizar) para, posteriormente, estilar los wireframes.

Por último, en algunos casos, se realiza una compilación de todos los elementos gráficos del sitio/app en un único archivo que se extiende como guía para nuevas decisiones de diseño relativas al producto que pudiera tener que tomar.

### Salidas

- Utilza un sistema estandar de wireframing.
- Corroborar alineación conforme a la grilla elegida para el desarrollo del trabajo. Ser consistente en el uso tipográfico (verificar coherencia entre estilos, legibilidad, etc.).
- Buscar concordancia estética con los guidelines de diseño de la empresa.
- Ser coherente con las necesidades/objetivos.
- Contemplar tipografías e imágenes a utilizar, comunicándole oportunamente que puede que tenga que comprar las respectivas licencias.
- Profundizar respecto a los estándares web y mobile al momento de realizarse el trabajo.
- Ser consistente respecto a las páginas presentadas. El cambio en alguna de las secciones compartidas (header, footer) debe repercutir necesariamente en todas las demás.
- Trabajar los archivos a tamaño real (en pixels) de acuerdo a la resolución del dispositivo de destino.
- Tratar de no utilizar texto o contenido simulado. De no existir material, deberán buscarse textos que se aproximen en su contenido a los que vayan a incluirse finalmente. Nunca uses lorem ipsum (salvo que sea para puro relleno).
- Contemplar los diferentes escenarios posibles a la hora de plantear un diseño con contenido que será dinámico. Prestá atención en particular a casos donde el texto pueda ser mucho más largo, ya que es algo que impacta mucho en la etapa de implementación.
- Generar propuesta justificando decisiones que evidencien criterio y buen gusto.
- Construir cada modulo por `Pages` de `Sketch`.
- Nombrar y organizar archivos siguiendo las pautas estipuladas.
- Corroborar que los archivos sean la versión aprobados.
- Ordenar prolijamente los elementos que hacen a los diferentes archivos en carpetas que identifiquen propiamente cada una de las secciones diseñadas. Los nombres de los elementos/carpetas deberán estar en inglés.
- Optimizar el peso de los archivos, eliminando todos aquellos elementos que no tengan razón de ser en el diseño final aprobado.
- Prestá particular atención para documentar animaciones, estados de hover y active para links, comportamiento del layout para diversos monitores (aclará qué tamaño tiene el diseño, si ocupa toda la pantalla o no, qué componentes quedan fijos, etc), y verificá los efectos a usar junto con un desarrollador para asegurarte de que puedan ser implementados correctamente.
