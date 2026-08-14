# Hola, soy Alan Acevedo

Desarrollador de Software Full-Stack en último año de formación.
Enfocado en construir aplicaciones web funcionales y APIs robustas.

---

## Sobre mí

Soy desarrollador con enfoque full-stack, especializado en backend con **Java y Spring Boot** y desarrollo de interfaces con **JavaScript y TypeScript**. Tengo experiencia construyendo APIs RESTful, modelando bases de datos relacionales y contenerizando aplicaciones con Docker. Incorporo herramientas de **Inteligencia Artificial** en mi flujo de trabajo para acelerar el desarrollo, mejorar la calidad del código y resolver problemas complejos de forma eficiente.

- 📍 Santa Fe, Argentina
- En curso: Último año en la Tecnicatura en Desarrollo de Software
- Abierto a oportunidades laborales y pasantías
- Contacto: [LinkedIn](https://www.linkedin.com/in/acevedo-alan/) · <Acevedo.j.Alan@gmail.com>

---

## Stack Tecnológico

**Backend**

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)

**Frontend**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

**Bases de Datos**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Herramientas y DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

---

## IA aplicada al desarrollo

Utilizo herramientas de IA de forma **proficiente** como parte activa de mi flujo de trabajo:

- **Generación y revisión de código**: uso de multiples agentes de Copilot y Claude para acelerar la escritura de lógica de negocio, detectar errores y refactorizar.
- **Diseño de arquitecturas**: validación de decisiones de diseño en APIs REST y estructura de base de datos.
- **Debugging asistido**: análisis de stack traces y errores complejos para reducir tiempos de resolución.
- **Documentación técnica**: generación y mejora de READMEs, comentarios de código y documentación de endpoints.

---

## Proyectos Destacados

### HEXA — Juego multijugador de matching de colores en tiempo real

> Proyecto propio · Full-stack, del diseño al deploy

Juego donde los jugadores reciben un color objetivo, salen a fotografiar objetos reales del mundo que lo matcheen, y compiten por precisión de color en tiempo real. Diseñado y desarrollado en solitario, de punta a punta.

- Sincronización de sala en tiempo real con **Server-Sent Events**, con reconexión automática ante pérdida de señal — elegido en vez de WebSockets por ser un flujo de datos mayormente unidireccional (servidor → jugadores), más liviano para una sesión efímera pensada para jugarse en LAN.
- Autenticación de sesión sin login tradicional: tokens firmados **HMAC-SHA256** (los jugadores se unen solo con un código de sala) + **rate limiting** sobre el endpoint de captura de fotos para evitar abuso.
- Diagnostiqué y resolví un fallo silencioso en producción: el backend guardaba fotos con datos corruptos cuando fallaba la subida a Cloudinary, sin reportar error al cliente. El fix usa rollback transaccional para que la operación falle de forma explícita en vez de dejar estado inconsistente en la base.
- Frontend **PWA** instalable (React + TypeScript + Vite), con generación de imágenes client-side vía **Canvas 2D** para exportar y compartir resultados sin depender de un servicio externo de renderizado.

[![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) [![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) [![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

🔗 [Repositorio](https://github.com/Acevedo-Alan/hex)

---

### RDAM — Registro de Deudores Alimenticios Morosos

> **Cliente:** Poder Judicial de Santa Fe · **Programa:** Campus 2026

Plataforma seleccionada entre los **8 finalistas** del programa Campus 2026 para la fase de evaluación final.

- Diseño e implementación de una **API RESTful** con Java y Spring Boot bajo arquitectura en capas (Controller → Service → Repository), para gestión de datos sensibles del Poder Judicial de Santa Fe.
- Autenticación de doble factor (**JWT + OTP**) en vez de sesiones tradicionales, dado que la plataforma maneja información de deudores alimenticios y requería una capa extra de verificación de identidad.
- Modelado y gestión de base de datos relacional con **PostgreSQL**, garantizando integridad referencial en los registros de deudores.
- Validación end-to-end de los endpoints con **Postman** antes de cada entrega, para sostener el flujo de datos cliente-servidor sin regresiones.

[![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) [![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) [![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

---

### OpenLodge

> **Proyecto académico colaborativo**

Aplicación full-stack desarrollada en equipo con flujo de trabajo profesional en Git.

- Construcción del frontend con **HTML5, CSS3, JavaScript y TypeScript**, conectado a la API mediante `fetch`/`axios`.
- Contenerización con **Docker** para estandarizar el entorno entre los miembros del equipo.
- Autenticación y autorización de usuarios con **Spring Security**.
- Gestión de ramas, pull requests y resolución de conflictos en **GitHub**.

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) [![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) [![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Acevedo_Alan-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/acevedo-alan) [![GitHub](https://img.shields.io/badge/GitHub-Acevedo--Alan-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Acevedo-Alan)
