<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com/?font=Fira+Code&size=28&pause=1000&color=F79839&width=520&lines=C%3A%5CUsers%5CAlan%3E+whoami;Alan+Acevedo;Full+Stack+Developer)](https://git.io/typing-svg)

</div>

# Hi, I'm Alan Acevedo

Full-Stack Software Developer in my final year of formal training.
Focused on building functional web applications and robust APIs.

---

## About me

I'm a full-stack developer specialized in backend with **Java and Spring Boot**, and interface development with **JavaScript and TypeScript**. I have experience building RESTful APIs, modeling relational databases, and containerizing applications with Docker. I actively incorporate **AI tools** into my workflow to speed up development, improve code quality, and solve complex problems efficiently.

- 📍 Santa Fe, Argentina
- Currently: Final year of the Software Development degree (Tecnicatura)
- Open to job opportunities and internships
- Contact: [LinkedIn](https://www.linkedin.com/in/acevedo-alan/) · <Acevedo.j.Alan@gmail.com>

---

## Tech Stack

**Backend**

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)

**Frontend**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Tools & DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

---

## AI applied to development

I use AI tools **proficiently** as an active part of my workflow:

- **Code generation and review**: using multiple Copilot and Claude agents to speed up business-logic writing, catch bugs, and refactor.
- **Architecture design**: validating design decisions for REST APIs and database structure.
- **Assisted debugging**: analyzing stack traces and complex errors to reduce resolution time.
- **Technical documentation**: generating and improving READMEs, code comments, and endpoint docs.

---

## Certifications

**Software Development with Claude Code** — DataCamp
Issued: August 2026 · Credential ID: `b318eed04cf43bde14c08ee08d6492cb342d0229`

---

## Featured Projects

### HEXA — Real-time color matching multiplayer game

> Solo project · Full-stack, from design to deploy

A game where players get a target color, go photograph real-world objects that match it, and compete on color-matching accuracy in real time. Designed and built solo, end to end.

- Real-time room sync via **Server-Sent Events**, with automatic reconnection on signal loss — chosen over WebSockets since the data flow is mostly one-directional (server → players), lighter weight for an ephemeral session meant to be played over LAN.
- Session auth without traditional login: **HMAC-SHA256**-signed tokens (players join with just a room code) + **rate limiting** on the photo-capture endpoint to prevent abuse.
- Diagnosed and fixed a silent production failure: the backend was saving photos with corrupted data whenever the Cloudinary upload failed, without surfacing an error to the client. The fix uses transactional rollback so the operation fails explicitly instead of leaving inconsistent state in the database.
- Installable **PWA** frontend (React + TypeScript + Vite), with client-side image generation via **Canvas 2D** to export and share results without relying on an external rendering service.

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

🔗 [Repository](https://github.com/Acevedo-Alan/hex)

---

### RDAM — Delinquent Support Debtors Registry

> **Client:** Judicial Branch of Santa Fe · **Program:** Campus 2026

Platform selected among the **8 finalists** of the Campus 2026 program for the final evaluation stage.

- Designed and implemented a **RESTful API** with Java and Spring Boot under a layered architecture (Controller → Service → Repository), for managing sensitive Judicial Branch data.
- Two-factor authentication (**JWT + OTP**) instead of traditional sessions, since the platform handles delinquent-debtor information and required an extra layer of identity verification.
- Modeled and managed a relational database with **PostgreSQL**, ensuring referential integrity across debtor records.
- End-to-end endpoint validation with **Postman** before every release, to keep the client-server data flow regression-free.

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

---

### OpenLodge

> **Collaborative academic project**

Full-stack application built as a team with a professional Git workflow.

- Built the frontend with **HTML5, CSS3, JavaScript and TypeScript**, connected to the API via `fetch`/`axios`.
- Containerized with **Docker** to standardize the environment across the team.
- User authentication and authorization with **Spring Security**.
- Branch management, pull requests, and conflict resolution on **GitHub**.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Acevedo_Alan-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/acevedo-alan) [![GitHub](https://img.shields.io/badge/GitHub-Acevedo--Alan-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Acevedo-Alan)
