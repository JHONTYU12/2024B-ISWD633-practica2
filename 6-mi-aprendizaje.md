# COMPLETAR

### Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.

Esta práctica me permitió profundizar en varios temas esenciales para gestionar contenedores Docker de manera eficaz, incluyendo el uso de **mapeos de puertos, variables de entorno, redes personalizadas y persistencia de datos mediante volúmenes**. A continuación detallo los aprendizajes logrados en cada uno de estos temas y su impacto en mi formación profesional.

#### Mapeo de Puertos
Aprendí cómo exponer servicios internos del contenedor, como WordPress, hacia el exterior utilizando el mapeo de puertos (`-p 9300:80`). Esto me ayudó a ver cómo los contenedores pueden mantener su configuración interna mientras asignan puertos específicos del host para acceder a sus servicios. Este conocimiento es fundamental para entornos de producción y desarrollo, ya que permite la interacción segura y controlada con aplicaciones que requieren acceso web.

#### Variables de Entorno
La práctica también me enseñó la importancia de configurar **variables de entorno** (`WORDPRESS_DB_HOST`, `WORDPRESS_DB_USER`, etc.) para personalizar contenedores según las necesidades de cada aplicación. En el caso de WordPress y MySQL, pude ver cómo estas variables controlan la conexión entre ambos servicios sin necesidad de modificar el código de las aplicaciones. La gestión de variables de entorno es especialmente útil para aplicar configuraciones consistentes y escalables en entornos de despliegue automatizado.

#### Redes en Docker
Crear y gestionar redes personalizadas en Docker fue otro tema clave. Al conectar WordPress y MySQL en una red compartida (`net-wp`), entendí cómo Docker permite la comunicación interna entre contenedores sin exponer sus puertos públicamente. Esto no solo mejora la seguridad del sistema, sino que facilita la escalabilidad, ya que los contenedores pueden comunicarse directamente mediante nombres de host en lugar de direcciones IP. Esta capacidad de crear redes internas es fundamental en arquitecturas de microservicios y en aplicaciones de múltiples componentes.

#### Persistencia de Datos con Volúmenes
Un aprendizaje clave fue el uso de **volúmenes en Docker para persistir datos**. Al experimentar con el reinicio de contenedores y observar que los datos se mantenían, entendí cómo los volúmenes almacenan información de manera independiente al ciclo de vida del contenedor. Esto es particularmente relevante en aplicaciones como WordPress, donde la configuración y los datos deben persistir entre reinicios. Sin embargo, también descubrí cómo eliminar volúmenes manualmente cuando se requiere una instalación limpia, un paso importante para evitar datos residuales no deseados.

### Solución de Problemas
Durante la práctica, enfrenté un problema donde el contenedor de WordPress mantenía configuraciones previas tras eliminarlo y recrearlo. Esto se debía a que Docker guardaba los datos en un volumen persistente, lo que me hizo investigar cómo gestionar estos volúmenes para controlar qué información conservar o eliminar. Finalmente, la solución fue eliminar el volumen asociado al contenedor para lograr una instalación completamente nueva. Esta experiencia me enseñó a identificar y resolver problemas de persistencia de datos, un aspecto crítico en la gestión de aplicaciones en contenedores.

### Impacto en mi Formación Profesional
Estos aprendizajes amplían mis habilidades para trabajar con contenedores de manera más segura y eficiente. Con el conocimiento de mapeos de puertos, redes personalizadas y persistencia de datos, puedo diseñar entornos de desarrollo y producción que son escalables, seguros y adaptables. La práctica también mejoró mi comprensión de la automatización y despliegue de aplicaciones distribuidas, lo que es esencial en entornos de trabajo modernos que utilizan contenedores y servicios en la nube.
