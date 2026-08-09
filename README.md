# ERP -  Product BackLog & UserStory

## Descripción

Este proyecto corresponde al desarrollo del taller de arquitectura de software (Product BackLog & UserStory)
para el diseño de un sistema ERP (Enterprise Resource Planning).

El objetivo es analizar y documentar una arquitectura de software orientada a
centralizar y gestionar diferentes procesos empresariales.

El ERP contempla los siguientes módulos:

- Módulo de Compras
- Módulo de Facturación
- Módulo de Stock/Costos
- Módulo de Activos Fijos
- Módulo de Empleados
- Módulo EIS

Para el desarrollo del taller se profundiza inicialmente en el **Módulo de
Compras**, donde se definieron historias de usuario, criterios de aceptación
y una propuesta de arquitectura para el sistema.

---

## Alcance del taller

El proyecto incluye:

- Definición de historias de usuario.
- Definición de criterios de aceptación.
- Priorización de historias mediante MoSCoW.
- Diseño de la arquitectura del sistema.
- Diagramas de arquitectura mediante PlantUML.
- Documentación de arquitectura utilizando arc42.
- Modelo de datos relacionado con el Módulo de Compras.
- Propuesta de despliegue de la solución.

---

## Arquitectura

Para el desarrollo del sistema ERP se propone una arquitectura web
monolítica, organizada en una aplicación frontend, una API REST para la
lógica de negocio y una base de datos relacional.

## Tecnologías

| Capa | Tecnología | Justificación |
|---|---|---|
| Frontend | React | Permite construir una interfaz basada en componentes reutilizables. |
| Build / Dev Server | Vite | Proporciona un entorno rápido para desarrollo y construcción del frontend. |
| Backend | Node.js | Permite ejecutar JavaScript en el servidor y utilizar un mismo lenguaje en frontend y backend. |
| Framework Backend | Express.js | Facilita la implementación de la API REST y la organización de las rutas y lógica del backend. |
| Base de datos | SQL Server | Proporciona almacenamiento relacional para gestionar los datos estructurados del ERP y mantener su integridad. |

## Documentación 

La documentación de arquitectura se encuentra en la carpeta ![Documentación](./docs)

## Diagramas

Los diagramas se encuentran en:![Diagramas](./docs/diagrams)

## Imagenes

Las imagnes generadas de los diagrmas se encuentran en:![Imagenes](./docs/images)
