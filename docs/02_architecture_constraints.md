# Restricciones de la Arquitectura {#section-architecture-constraints}

## Decisiones Arquitectónicas

Para el desarrollo del sistema ERP se propone una arquitectura web
monolítica, organizada en una aplicación frontend, una API REST para la
lógica de negocio y una base de datos relacional.

La arquitectura se selecciona como una decisión inicial orientada a mantener una estructura clara y cohesiva del sistema, facilitando la integración de los módulos del ERP y su evolución progresiva a medida que aumenten los requerimientos funcionales y no funcionales.

### Arquitectura monolítica

El sistema se implementará inicialmente como una aplicación monolítica.
Los principales componentes del sistema estarán integrados dentro de una
misma solución, facilitando su desarrollo y despliegue.

### API REST

El backend expondrá servicios mediante una API REST. Esta decisión permite
separar la interfaz de usuario de la lógica de negocio y facilita la
comunicación entre el frontend y otros sistemas externos.

## Tecnologías

| Capa | Tecnología | Justificación |
|---|---|---|
| Frontend | React | Permite construir una interfaz basada en componentes reutilizables. |
| Build / Dev Server | Vite | Proporciona un entorno rápido para desarrollo y construcción del frontend. |
| Backend | Node.js | Permite ejecutar JavaScript en el servidor y utilizar un mismo lenguaje en frontend y backend. |
| Framework Backend | Express.js | Facilita la implementación de la API REST y la organización de las rutas y lógica del backend. |
| Base de datos | SQL Server | Proporciona almacenamiento relacional para gestionar los datos estructurados del ERP y mantener su integridad. |

## Restricciones Tecnológicas

- El frontend utilizará React y Vite.
- El backend utilizará Node.js y Express.js.
- La comunicación entre frontend y backend se realizará mediante una API REST.
- La información persistente será almacenada en SQL Server.
- La solución utilizará inicialmente una arquitectura monolítica.