# Guía de Onboarding Técnico para Nuevos Ingresos

## Introducción

Este documento tiene como propósito servir de guía de **onboarding técnico** para nuevos integrantes del equipo de desarrollo. Aquí se detallan todos los pasos necesarios para configurar el entorno de trabajo, obtener los accesos requeridos y preparar las herramientas indispensables, de modo que el nuevo ingreso pueda comenzar a trabajar en el proyecto sin inconvenientes. El contenido está estructurado paso a paso y con ejemplos, utilizando un tono formal y proporcionando capturas de pantalla ilustrativas para facilitar el seguimiento.

## Accesos requeridos y cómo solicitarlos

En esta sección se enumeran los accesos que todo nuevo integrante debe obtener, junto con las instrucciones para solicitarlos. Para cada tipo de acceso, se indica el proceso a seguir, un ejemplo de solicitud (en caso de que se deba enviar un correo o ticket), y se reserva un espacio para insertar una captura de pantalla de referencia.

### Acceso a Jira / Confluence:

Link Jira:
Link Confluence:

**Paso a paso para solicitar acceso a Jira:**

_(Inserte aquí una captura de pantalla de ejemplo del formulario o correo de solicitud de acceso a Jira)_

### Acceso a servidores de producción y UAT/CAT

Para interactuar con los **servidores de producción**, generalmente se requiere un acceso restringido que debe ser aprobado por varios responsables, dado que involucra sistemas críticos. Es importante seguir el procedimiento establecido para obtener credenciales o permisos de conexión.

**Paso a paso para solicitar acceso a servidores de producción:**

1. **Completar el request de solicitud:** 
    
2. **Proporcionar detalles requeridos:** 
        
3. **Revisión y aprobación:** 
    

**Ejemplo de datos en la solicitud:** 

_(Inserte aquí una captura de pantalla del sistema de solicitud de accesos, mostrando un ejemplo de petición de acceso a un servidor de producción)_

### Acceso a base de datos

El acceso a la **base de datos** del proyecto es esencial para ejecutar consultas, depurar datos o verificar configuraciones. Por motivos de seguridad, las credenciales de base de datos suelen manejarse con cuidado, asignando privilegios según el entorno (producción, pruebas, desarrollo).

**Paso a paso para solicitar acceso a la base de datos:**


_(Inserte aquí una captura de pantalla del panel de administración de la base de datos o del correo de confirmación con las credenciales, ocultando datos sensibles)_

### Creación de cuentas necesarias

Además de los accesos a sistemas mencionados, es importante verificar que el nuevo integrante cuenta con todas las **cuentas de usuario** necesarias para trabajar. A continuación se listan las cuentas típicas y cómo obtenerlas en caso de que no se hayan creado automáticamente durante el proceso de ingreso:

| **Cuenta / Sistema**             | **Descripción y uso**                                                                                                                         | **Cómo obtener / solicitar**                                                                                                                    |
| -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cuenta de correo corporativo** | Dirección de email de la empresa, necesaria para comunicaciones internas y registro en herramientas.                                          | Creada por TI al ingreso. Si no está activa, contactar a Mesa de Ayuda.                                                                         |
| **Cuenta de dominio (AD)**       | Credenciales de red/Windows (Active Directory) para iniciar sesión en el equipo y acceder a recursos internos.                                | Creada por TI al ingreso (usuario y contraseña inicial provistos). Solicitar reset si hay problemas de acceso.                                  |
| **Jira y Confluence**            | Usuario para seguimiento de tareas (Jira) y documentación interna.                                                                            | Solicitar al administrador Atlassian (ver sección de acceso a Jira). Generalmente se usa el correo corporativo.                                 |
| **Repositorio de código (Git)**  | Acceso al control de versiones (Bitbucket, GitLab o GitHub Enterprise, según aplique). Permite clonar/push el código fuente.                  | Solicitar invitación al administrador de repositorios. Proveer correo corporativo y nombre de usuario deseado.                                  |
| **Herramientas de CI/CD**        | Cuenta en las herramientas de Integración Continua/Despliegue Continuo (por ej., Jenkins, Azure DevOps, GitLab CI).                           | Solicitar al DevOps o administrador de la herramienta. A veces se integra con la cuenta de dominio.                                             |
| **Otros accesos específicos**    | Cualquier otra cuenta relacionada al proyecto (p. ej., acceso a una API externa, cuenta en herramienta de monitoreo o bug tracking distinto). | Verificar con el líder de proyecto y el checklist de onboarding. Solicitar según el caso (puede ser vía correo o tickets a diferentes equipos). |

## Herramientas y programas necesarios

En esta sección se detallan las distintas herramientas de software que el desarrollador debe instalar o tener acceso para trabajar eficientemente en el proyecto. Para cada herramienta se indica su propósito, cómo obtenerla (ya sea descarga directa o a través del centro de software corporativo), pasos básicos de instalación y configuración, así como recomendaciones particulares (por ejemplo, plugins útiles o ajustes iniciales). También se proveen capturas de pantalla de ser pertinente para guiar en la instalación o reconocimiento de la interfaz.

### IntelliJ IDEA (IDE de Desarrollo)

### Postman Enterprise (Cliente API)


- **Obtención:** Postman puede instalarse desde el **Software Center** (buscar "Postman Enterprice") 
- 
- **Licencia/Acceso Enterprise:** Luego de instalar, realizar el siguiente request:

    

_(Inserte aquí una captura de pantalla de Postman mostrando una petición de ejemplo a la API, con la URL y parámetros configurados)_

Acceso a servidores:
### MobaXterm (Cliente SSH y herramientas remotas)

**MobaXterm** es una suite de terminal con cliente SSH, X11 y otras utilidades, útil para conectarse a servidores Linux/Unix de forma remota desde Windows. Incluye un emulador de terminal con pestañas, un explorador SFTP integrado y soporte para túneles SSH entre otras funciones.

_(Inserte aquí una captura de pantalla de MobaXterm con una sesión SSH abierta, mostrando el terminal conectado a un servidor y el panel lateral de SFTP)_

### PuTTY (Cliente SSH alternativo)

**PuTTY** es un cliente SSH y telnet ligero. Aunque MobaXterm ofrece más funcionalidades, PuTTY es una alternativa sencilla para conexiones SSH directas, y suele ser utilizada si se requieren herramientas puntuales como _PuTTYgen_ (generador de claves) o _Pageant_ (agente de autenticación).



### WinSCP (Cliente SFTP/FTP)

_(Inserte aquí una captura de pantalla de WinSCP mostrando la interfaz de doble panel con una conexión establecida a un servidor remoto)

 **Obtención:** Disponible en el **Software Center**.
    
- **Prerequisitos:** Para utilizar estos programas es necesario obtener el acceso a los servidores, para servidores de produccion utilizar el usuario "Z", para servidores de UAT utilizar el usuario "W", estos usuarios se encuentran en Cyberark
- Link de cyberark:
- Link de request:

### MySQL Workbench (Administración de Base de Datos MySQL)

**MySQL Workbench** es la herramienta oficial de MySQL para diseño y administración de bases de datos, que permite conectarse a instancias MySQL/MariaDB para ejecutar consultas SQL, diseñar esquemas y gestionar datos de forma visual. Es fundamental para interactuar con la base de datos del proyecto _XYZ_.

- **Obtención:** Disponible en **Software Center** como "MySQL Workbench".
        
- **Usuarios de servicio disponibles:** La empresa dispone de ciertos usuarios predefinidos para la base de datos:
    
    - Por ejemplo, un usuario de **solo lectura** (`xyz_readonly`) para consultas y análisis, y otro de **lectura/escritura** (`xyz_dev`) para uso en desarrollo/UAT. En producción, típicamente solo se utiliza el de solo lectura para indagar datos (las escrituras en producción las hace la aplicación misma).
        
    - Estos usuarios y sus contraseñas son gestionados por el DBA. Si se le otorgó uno de ellos, úselo en lugar de su cuenta personal para conectarse, según el caso. **Nota:** Nunca utilizar cuentas con privilegios elevados en entornos sensibles sin autorización.
    
IMB DATA STUDIO:

Obtención: Disponible en Software Center, para instalarlo hay que instalar previamente los siguientes programas: Buscar IMB e instalar: xxxx,xxx,xxx,xx



## Soporte

Ante cualquier inconveniente, duda o problema durante el proceso de onboarding técnico, el nuevo integrante puede recurrir a los canales de soporte disponibles. En particular, la empresa cuenta con un canal de **Microsoft Teams** dedicado a asistencia en IT llamado _“itchat”_.

Allí podrá plantear preguntas en tiempo real y obtener ayuda del equipo de soporte o de compañeros con experiencia. Se recomienda, al pedir ayuda, brindar detalles específicos (por ejemplo, adjuntar captura de pantalla del error, indicar qué paso del onboarding presentó el inconveniente, etc.) para facilitar y agilizar la respuesta.




Desarrollo y Entrega de Sistemas | Etapas de Control (PTX Tollgates)

Asegurar que los requerimientos fundamentales de ciberseguridad y controles tecnológicos se cumplan en puntos clave del ciclo de vida del proyecto.


---

Permiso para Diseñar

Se ha completado la recolección de requisitos y se autoriza la asignación de recursos

Controles de Ciberseguridad

Completar Encuesta de Seguridad y Control de IT (en ServiceNow)

Clasificación de la Aplicación asignada

Clasificación de Datos asignada


Controles Tecnológicos

Aprobación completa del portafolio de proyectos

Capturar APM# con asignación de propietario de activo (en ServiceNow)

Asignar Estrategia de Recuperación, Objetivo de Tiempo de Recuperación, Objetivo de Punto de Recuperación

Involucrar cumplimiento regulatorio del producto (aplicable a ciertos tipos de proyectos)



---

Permiso para Construir

Validar que el diseño del sistema incluye requerimientos de ciberseguridad y control tecnológico

Controles de Ciberseguridad

Completar Evaluación de Impacto de Seguridad de Software (SSIA)

Escaneos de Vulnerabilidades

Encriptación de Datos

Autenticación Fuerte (MFA)

Firewall de Aplicaciones Web

Registro (Logging)

Aprovisionamiento Automático

Seguridad en la Nube


Controles Tecnológicos

Revisión completa de arquitectura

Obtener aprobación del diseño



---

Permiso para Operar

Las pruebas se han completado y se cumplen los requerimientos de ciberseguridad y controles tecnológicos

Controles de Ciberseguridad

Entregar controles fundamentales:

Encriptación de Datos

Vulnerabilidades

Autenticación Fuerte (MFA) (Nuevo)

Firewall de Aplicaciones Web (Nuevo)



Controles Tecnológicos

Presentar los artefactos obligatorios del Documento de Diseño del Sistema (SDD)



---

Permiso para Operar - Etapa de Control

Integrado con el proceso de Gestión de Cambios de Fiserv y el flujo de trabajo en ServiceNow

Si un proyecto no cumple con los requerimientos del "Permiso para Operar", la solicitud de cambio a producción se pausa hasta que se resuelva la excepción mediante corrección o tratamiento del riesgo
