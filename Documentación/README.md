# Documentación

En el diseño arquitectónico anterior se puede observar que se utilizó la arquitectura de microservicios. Se decidió utilizar este tipo de arquitectura ya que permite eliminar o al menos mitigar los problemas que causaba la estructura monolítica en mediación virtual. Además, de que es una de las arquitecturas más importantes y fáciles de crear un diseño arquitectónico debido a la buena cantidad de ejemplos que hay en internet y las excelentes explicaciones del experto en patrones y arquitecturas de diseño Martin Fowler. Más adelante se especificarán los beneficios, desafíos y comparaciones entre la arquitectura monolítica de mediación virtual y el diseño arquitectónico planteado para que se logre comprender mejor el porqué se eligió esta arquitectura.

La estructura monolítica agrupa todas las funcionalidades y servicios de un sistema en una unidad o base de código. Es decir, todas las capas del sistema, la interfaz del usuario (UI) y la base de datos se encuentran en un solo lugar y dependen unas con otras. Esto quiere decir que, si se desea cambiar alguna funcionalidad en el sistema de mediación virtual, puede afectar a toda la estructura y puede requerir una nueva compilación y despliegue de toda la aplicación. Esto puede resultar en un proceso de desarrollo y despliegue lento y costoso, especialmente a medida que la aplicación crece y se vuelve más compleja [3].

Ya que la mediación virtual es un sistema universitario grande, es más viable utilizar la arquitectura de micro servicios en lugar de la arquitectura monolítica. Según Martin Fowler, el estilo arquitectónico de microservicios es un enfoque utilizado para desarrollar una sola aplicación como un conjunto de pequeños servicios, cada uno ejecutándose en su propio proceso y comunicándose con mecanismos livianos, a menudo una API de recursos HTTP (o usando el API Gateway). Estos servicios se basan en capacidades comerciales y se implementan de forma independiente mediante maquinaria de implementación totalmente automatizada. Hay un mínimo indispensable de gestión centralizada de estos servicios, que pueden estar escritos en diferentes lenguajes de programación y utilizar diferentes tecnologías de almacenamiento de datos [2].

Siguiendo la idea de Martin Fowler, a lo que se quiere llegar al implementar una arquitectura de microservicios es en separar las funciones de la aplicación en pequeños servicios independientes que se pueden desarrollar, probar y desplegar de forma individual permitiendo una mayor flexibilidad, escalabilidad y resiliencia en el desarrollo y despliegue de aplicaciones. Y aunque la arquitectura monolítica sea fácil de implementar y buena para aplicaciones pequeñas, lo cierto es que mediación virtual debe dejar de lado este tipo de arquitectura ya que a medida que avanza el tiempo, esta se va volviendo obsoleta debido a que todos los sistemas (incluyendo mediación virtual y otras plataformas universitarias de la UCR) van creciendo en complejidad, cargas de trabajo, número de desarrolladores y usuarios.

Como se mencionó anteriormente, el diagrama utiliza una arquitectura de microservicios para obtener diversos beneficios frente a la monolítica, entre los **BENEFICIOS** se encuentra:

* **Flexibilidad**: Permite a los desarrolladores trabajar en diferentes microservicios de forma independiente, lo que facilita la implementación de cambios en el código y la introducción de nuevas funcionalidades sin afectar a otros servicios. Esto también facilita el mantenimiento y la actualización de los servicios de mediación virtual [1].

* **Resiliencia**: Al utilizar una arquitectura de microservicios, si un servicio falla, no afectará a los demás servicios en la aplicación. Además, esta arquitectura permite una mayor recuperación ante fallos ya que cada servicio implementado tiene sus propias medidas de restauración específicas.

* **Diversidad tecnológica**: Con los microservicios se pueden combinar varios lenguajes, marcos de desarrollo y tecnologías de almacenamiento de datos permitiendo que los desarrolladores utilicen las herramientas adecuadas para cada tarea y que cada uno de ellos pueda aprovechar sus habilidades en cada tecnología [1].

* **Desarrollo rápido**: Al trabajar en microservicios independientes, los desarrolladores pueden implementar y desplegar nuevas funcionalidades y servicios de forma más rápida y ágil.

Si bien la arquitectura de microservicios tiene ventajas muy buenas frente a la arquitectura monolítica, también tiene sus **DESAFIOS** o desventajas, en donde se puede mencionar:

* **Dificultad** de implementación: La arquitectura de microservicios, a diferencia de la arquitectura monolítica donde todo el código está en una sola aplicación, puede ser más complicada de implementar ya que se trata de un sistema distribuido. Esto implica que se deben desplegar y configurar múltiples componentes, lo cual puede generar una mayor complejidad en el manejo del sistema. Además, las llamadas remotas que se realizan entre los diferentes microservicios pueden ser lentas y corren el riesgo de fallar, lo que puede generar problemas en el rendimiento y la disponibilidad del sistema en general [1].

* **Costos**: La implementación de la arquitectura de microservicios en mediación virtual puede ser costosa debido a la necesidad de múltiples infraestructuras, herramientas y recursos para mantener los servicios en ejecución.

* **Complejidad operativa**: Para poder implementar el diseño arquitectónico de mediación virtual utilizando la arquitectura de microservicios se requiere de un equipo de operaciones experimentado y maduro capaz de administrar múltiples servicios y gestionar su despliegue regular.Esto se debe a que los sistemas con esta arquitectura tienen una mayor tasa de actualizaciones que la arquitectura monolítica por lo que se necesita un mayor esfuerzo en la gestión del control de versiones [1].

Otro aspecto importante que se le desea dar énfasis es en las capas del sistema en el diagrama realizado, se especificó cada capa del sistema como una forma de separar y organizar cada uno de los componentes del diseño arquitectónico.
En la capa de presentación se encuentra el UI (User Interface) que se encarga de presentar de forma más sencilla y amigable la información que solicita y es la que se comunica con el usuario directamente por medio de elementos gráficos como ventanas, botones, etc.

En la capa de aplicación se encuentran los controladores que permiten a la aplicación interactuar con la capa de servicios y con la capa de datos y proporcionar la funcionalidad que pidió el usuario en la capa de presentación.

En la capa de servicios se encuentran las funcionalidades que ofrece mediación virtual y pueden ser simples o complejos. Además, ayuda a separar las responsabilidades y a tener una arquitectura más modular y escalable.

Y, por último, se encuentra la capa de datos la cual se encarga de almacenar la información relevante de cada servicio y velar por la consistencia de los datos, así como de su seguridad y privacidad. Si varios microservicios comparten una base de datos, cualquier cambio en la estructura de la base de datos puede afectar a varios servicios. Es por eso que se decidió utilizar una base de datos separada para cada microservicio ya que se pueden hacer cambios en la estructura de la base de datos de un microservicio sin afectar a los otros microservicios.

# Bibliografía

[1] Microservices Guide. (s.f.). martinfowler.com. Disponible en: https://martinfowler.com/microservices/

[2] O'Reilly. (2015, 23 de julio). Making Architecture Matter - Martin Fowler Keynote [Video]. YouTube. https://www.youtube.com/watch?v=DngAZyWMGR0

[3] DevOps: Arquitectura monolítica vs Microservicios - Chakray. (s.f.). Chakray. Disponible en: https://www.chakray.com/es/devops-arquitectura-monolitica-vs-microservicios/
