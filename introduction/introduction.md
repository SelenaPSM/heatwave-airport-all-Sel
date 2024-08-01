# Introducción

![mysql heatwave](./images/mysql-heatwave-logo.jpg "mysql heatwave")

## Acerca de este Workshop

MySQL HeatWave es un servicio de base de datos totalmente gestionado con un acelerador de consultas integrado que permite a las organizaciones ejecutar de manera eficiente el procesamiento de transacciones, el análisis en tiempo real, el almacén de datos y el aprendizaje automático en los datos almacenados dentro de la base de datos MySQL o en el almacén de objetos.

MySQL HeatWave elimina la necesidad de operaciones ETL complejas para mover datos de MySQL para ejecutar análisis o aprendizaje automático. Las aplicaciones MySQL existentes se pueden ejecutar en MySQL HeatWave sin ningún cambio y obtener órdenes de magnitud para mejorar el rendimiento de las consultas con el acelerador de consultas integrado. Con MySQL HeatWave, las organizaciones también pueden ejecutar análisis en cientos de terabytes de datos en el almacén de objetos en una variedad de formatos de archivo como CSV, Parquet, exportar archivos desde Aurora o Redshift, sin necesidad de almacenar datos en MySQL.

En este taller, aprenderá a crear un cluster de MySQL HeatWave, conectarse al cluster mediante MySQL Shell, ejecutar consultas en HeatWave, ejecutar cargas de trabajo de Analytics en Oracle Cloud y crear una aplicación LAMP.

En general, este taller te mostrará lo fácil que es crear y gestionar MySQL HeatWave y cómo MySQL HeatWave te permite tomar decisiones empresariales críticas con conocimiento de causa y en tiempo real.

_Tiempo de laboratorio estimado:_ 1,5 horas

## Acerca del Producto/Tecnología

MySQL HeatWave es un acelerador de consultas en memoria, masivo y paralelo de alto rendimiento para Oracle MySQL Database Service que acelera el rendimiento de MySQL por órdenes de magnitud para análisis y cargas de trabajo mixtas. Es el único servicio que permite a los clientes ejecutar cargas de trabajo OLTP y OLAP directamente desde su base de datos MySQL sin la necesidad de un proceso ETL. MySQL Autopilot utiliza técnicas avanzadas de aprendizaje automático para automatizar las operaciones del ciclo de vida de la base de datos, incluido el aprovisionamiento, la carga de datos, el procesamiento de consultas y el manejo de errores. Esto minimiza el trabajo administrativo manual y mejora aún más la facilidad de uso, el rendimiento y la escalabilidad de HeatWave. MySQL HeatWave también se integra con otros servicios de Oracle Cloud como Data Integration Service y Oracle Analytics Cloud para proporcionar una integración completa y perfecta.

MySQL Database Service con HeatWave es un servicio totalmente gestionado, optimizado para Oracle Cloud Infrastructure. Le permite:

- Aprovisione al instante instancias de MySQL y conéctese a una base de datos MySQL preconfigurada y lista para producción.
- Ejecute la carga de trabajo OLTP y OLAP directamente en una única plataforma MySQL sin necesidad de ETL, y sin cambios en sus aplicaciones.
- Ejecutar eficazmente cargas de trabajo mixtas y analíticas con la mejor relación precio-rendimiento. HeatWave es 6.5X más rápido que Amazon Redshift a la mitad del costo, 7 veces más rápido que Snowflake a una quinta parte del costo y 1400 veces más rápido que Amazon Aurora a la mitad del costo.
- Tome decisiones empresariales más informadas obteniendo información en tiempo real de sus datos operativos.
- Libere tiempo de actividad de desarrolladores, administradores de bases de datos y DevOps para centrarse en tareas de valor agregado que son fundamentales para su negocio.
- Acceso a docenas de servicios adicionales de Oracle Cloud Services que permiten a las organizaciones adoptar el cambio a la nube.

_Configuración de laboratorio_

![heatwave architecture](./images/heatwave-bastion-architecture-compute.png "heatwave bastion -architecture compute ")


## Objetivos

En este Workshop, se le guiará por los siguientes pasos:

- Crear clave SSH en Oracle Cloud Infrastructure Cloud Shell
- Configuración de un ambiente OCI
- Creación de una instancia única del MySQL Database Service, conectando con SSH y MySQL Shell
- Conéctese al sistema de base de datos mediante MySQL Shell y agregue datos de ejemplo
- Cargar datos de ejemplo en el cluster HeatWave
- Ejecute consultas en HeatWave y MySQL y vea la mejora del rendimiento en HeatWave
- Creación de una aplicación PHP MySQL utilizando HeatWave
- Uso de Oracle Anayltics Cloud con MySQL HeatWave

## Pre-requisitos

- Una cuenta de prueba o de pago de Oracle Cloud Infraestructure 

Ahora puede **proceder al siguiente laboratorio**

## Créditos

- **Autor(es)** - Perside Foster, MySQL Principal Solution Engineering; Selena Sánchez, MySQL Solution Engineering
- **Colaboradores** - 
- **Última actualización** - Selena Sánchez, MySQL Solution Engineering, Agosto 2024
