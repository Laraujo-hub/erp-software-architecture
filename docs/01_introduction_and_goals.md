# Introducción y Metas {#section-introduction-and-goals}

El presente documento describe la arquitectura de un sistema ERP orientado a
centralizar y gestionar los principales procesos operativos de una empresa.

El sistema contempla los módulos de Compras, Facturación, Stock/Costos,
Activos Fijos, Empleados y EIS. Para este proyecto se profundiza inicialmente
en el Módulo de Compras, definiendo sus principales funcionalidades,
requerimientos y relaciones con los demás elementos del sistema.

## Vista de Requerimientos {#_vista_de_requerimientos}

El Módulo de Compras tiene como objetivo permitir la gestión de las
necesidades de adquisición de la empresa, desde la solicitud de productos
hasta su recepción.

Los principales requerimientos funcionales identificados son:

- Registrar y consultar productos.
- Registrar y consultar proveedores.
- Crear solicitudes de compra.
- Generar órdenes de compra.
- Registrar la recepción de mercancía.
- Consultar el estado de las solicitudes de compra.
- Mantener actualizada la información relacionada con las compras.

Estos requerimientos fueron definidos mediante historias de usuario y
criterios de aceptación gestionados en Jira.

## Metas de Calidad {#_metas_de_calidad}

Las principales metas de calidad consideradas para la arquitectura son:

+-----------------------+-------------------------------------------------------------------------------------------------------+
| Atributo de calidad   | Meta                                                                                                  |
+=======================+=======================================================================================================+
| Usabilidad            | Proporcionar una interfaz sencilla e intuitiva para los usuarios.                                     |
+-----------------------+-------------------------------------------------------------------------------------------------------+
| Mantenibilidad        | Mantener una estructura organizada que facilite la modificación y evolución del sistema.              |
+-----------------------+-------------------------------------------------------------------------------------------------------+
| Escalabilidad         | Permitir la incorporación de nuevos módulos y funcionalidades.                                        |
+-----------------------+-------------------------------------------------------------------------------------------------------+
| Seguridad             | Proteger la información y controlar el acceso a las funcionalidades del ERP.                          |
+-----------------------+-------------------------------------------------------------------------------------------------------+
| Rendimiento           | Proporcionar tiempos de respuesta adecuados en las operaciones principales.                           |
+-----------------------+-------------------------------------------------------------------------------------------------------+
| Integridad de datos   | Garantizar la consistencia de la información mediante una base de datos relacional y transacciones.   |
+-----------------------+-------------------------------------------------------------------------------------------------------+


## Partes interesadas (Stakeholders) {#_partes_interesadas_stakeholders}


+---------------------------------------------+-------------+------------------------------------------------------------+
| Rol/Nombre                                  | Contacto    | Expectativas                                               |
+=============================================+=============+============================================================+
| Administrador del sistema ERP               | Por definir | Gestionar y supervisar los módulos y usuarios del sistema. |
+---------------------------------------------+-------------+------------------------------------------------------------+
| Gestor de compras                           | Por definir | Gestionar proveedores, solicitudes y órdenes de compra.    |
+---------------------------------------------+-------------+------------------------------------------------------------+
| Gestor de inventario                        | Por definir | Mantener actualizado el catálogo de productos y 
<br>controlar la  información relacionada con inventario<br>                                                             |
+---------------------------------------------+-------------+------------------------------------------------------------+
| Empleado solicitante                        | Por definir | Registrar y consultar solicitudes de compra.               |
+---------------------------------------------+-------------+------------------------------------------------------------+
| Responsable de recepción                    | Por definir | Registrar la recepción de mercancía y verificar las 
<br>cantidades recibidas.<br>                                                                                            |
+---------------------------------------------+-------------+------------------------------------------------------------+