# Framework Hibernar - Descripción general
------------------------------------------
https://www.tutorialspoint.com/hibernate/hibernate_overview.htm

Hibernate es una solución de mapeo relacional de objetos (ORM) para JAVA. Es un marco persistente de código abierto creado por Gavin King en 2001. Es un servicio de consulta y persistencia relacional de objetos potente y de alto rendimiento para cualquier aplicación Java.

Hibernate asigna clases de Java a tablas de bases de datos y de tipos de datos de Java a tipos de datos de SQL y libera al desarrollador del 95% de las tareas de programación comunes relacionadas con la persistencia de datos.

## Conexión mediante JDBC, Hibernate a base de datos HSQLDB (HyperSQL DataBase)
------------------------------------------------------------------------------
https://stackoverflow.com/questions/3807503/what-is-the-purpose-of-two-config-files-for-hibernate/3808406#3808406

Si está utilizando la API patentada de Hibernate, necesitará hibernate.cfg.xml. Si está utilizando JPA, es decir, Hibernate EntityManager, necesitará persistence.xml.

Por lo tanto, generalmente no necesita ambos, ya que utiliza la API patentada de Hibernate o JPA.

Sin embargo, si estaba utilizando la API patentada de Hibernate y ya tiene hibernate.cfg.xml (y archivos de mapeo XML hbm.xml) pero desea comenzar a usar JPA, puede reutilizar los archivos de configuración existentes haciendo referencia a hibernate.cfg.xml en el persistence.xml en la propiedad hibernate.ejb.cfgfile y, por lo tanto, tendrá ambos archivos. Reutilizar archivos hbm.xml existentes es, en mi opinión, un escenario realista que podría justificar conservar ambos (incluso si probablemente migraría a anotaciones JPA a largo plazo).

***
Nota: Si utiliza 'Hibernate.cfg.xml' la conexión es mediante 'SessionFactory' o 
      si utiliza 'persistence.xml' la conexion es mediante 'EntityManagerFactory'
***
