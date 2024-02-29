# Proyecto de gestion de desarrollo de software

Este proyecto fue creado por **Dylan perez**. para el proyecto del primer corte de la materia Arquitectura de Software, de la Universidad Jorge tadeo Lozano. Me costó muchísimo hacerlo y sé que faltan cosas, pero hice un gran esfuerzo, hace años no tocaba una línea de código y aunque sé que Java no es el lenguaje mas amigable para un proyecto como este, lamentablemente no conozco medianamente otro lenguaje tanto como Java


# Archivos

La base de datos está definida como "**ddl.sql**" y los registros base están incluidos como un fichero sql también, llamado:  **data.sql**

## Entorno de desarrollo

Este proyecto fue desarrollado con lenguaje Java, y persistencia en base de datos relacional MySQL de cliente Xampp. Se utilizó IDE Sprong tool suite 4, gestor de paquetes Maven y Spring Boot como gestor de proyecto, en adición, se utilizó JPA como ORM y Hibernate, para asistir el mapeo de la base de datos. Se probo en un entorno local con ** base de datos de usuario "root" y contraseña: "" (Vacía)**

## ROLES de usuario

Se logro incluir roles de Desarrollador: "**ROLE_DEV**" y de Gerente: "**ROLE_MGR**". Así mismo, mediante de anotaciones en los controladores se limitó el acceso de ciertos métodos segun el rol de usuario, aunque desafortunadamente no se configuró ningun mensaje personalizado.

	> @Secured("ROLE_DEV")
	> @Secured("ROLE_MGR")
y para autorizar permisos a ambos: 

	> @Secured({"ROLE_MGR", "ROLE_DEV"})
