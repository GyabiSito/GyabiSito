# 👋 ¡Hola! Soy José Gabriel Hernández (GyabiSito)

📍 Desde Montevideo, Uruguay | 💻 Desarrollador orientado a seguir aprendiendo, metiendo mano y mejorando cada día.

Me encanta meterme en el código, entender cómo funciona todo desde adentro y compartir lo que voy aprendiendo. Estoy explorando distintas tecnologías — desde Java hasta Laravel, pasando por Gherkin, Selenium, C++ y Angular

---





## 🛠️ Tecnologías con las que estoy trabajando o aprendiendo

![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-E74430?style=flat-square&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Gherkin](https://img.shields.io/badge/Gherkin-5FB518?style=flat-square)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)

---
## Proyectos Productivos

### 🌿 Komorebi — E-commerce Full Stack
[Komorebi](https://komorebi.com.uy/)

> 🛒 E-commerce real • 💳 MercadoPago • ⚡ Redis y colas • 🐳 Docker • 🚀 Producción

**Komorebi** es una plataforma e-commerce full stack desarrollada para un cliente real, con una arquitectura separada entre la tienda pública, el panel administrativo y una API backend.

El proyecto cubre el flujo completo de una tienda online: catálogo, usuarios, carrito, compras, pagos, stock, gestión administrativa, notificaciones y operación en infraestructura real.

Además del desarrollo funcional, trabajé sobre aspectos de **autenticación, procesamiento asíncrono, webhooks de pago, correos transaccionales, seguridad, despliegue con Docker y configuración de reverse proxy**.

#### 🔧 Stack y arquitectura

* **Store:** Angular
* **Panel administrativo:** Angular
* **Backend:** Laravel + API REST
* **Base de datos:** PostgreSQL
* **Redis:** cache, colas y soporte para procesos asíncronos
* **Workers y Scheduler:** procesamiento de jobs y tareas programadas
* **MercadoPago:** checkout y confirmación de pagos mediante webhooks
* **SMTP2GO:** envío de correos transaccionales y administrativos
* **Docker:** servicios contenerizados para desarrollo y producción
* **Nginx:** reverse proxy y gateway de entrada
* **Infraestructura:** Hetzner VPS + Cloudflare

#### 🎯 Funcionalidades principales

* 🛍️ Catálogo y navegación de productos
* 🔎 Búsqueda y filtrado
* 👤 Registro, login y gestión de cuenta
* 🛒 Carrito de compras
* 💳 Integración con MercadoPago
* 🔔 Confirmación de pagos mediante webhooks
* 📦 Gestión de pedidos y estados
* 📊 Panel administrativo
* 🏷️ Gestión de productos, categorías y stock
* 📈 Métricas e información comercial para administración
* ✉️ Correos transaccionales y notificaciones administrativas
* ⚡ Procesamiento asíncrono mediante Redis y queues
* 🔐 Autenticación y autorización entre Store, Admin y API
* 🐳 Deployment reproducible mediante Docker

#### 🧠 Algunos desafíos técnicos

Uno de los puntos más importantes fue diseñar correctamente el flujo de compra para que el estado del pedido no dependa únicamente de lo que ocurre en el navegador.

La confirmación del pago se procesa desde backend mediante **webhooks de MercadoPago**, permitiendo actualizar pedidos y stock de forma confiable incluso cuando el usuario cierra la página o la respuesta del checkout no vuelve correctamente al frontend.

También se trabajó sobre:

* separación entre Store, Admin y API;
* manejo de autenticación y autorización;
* sincronización de stock después de las compras;
* jobs y tareas programadas fuera del request HTTP;
* correos de confirmación y notificaciones administrativas;
* despliegue de múltiples servicios Docker;
* configuración de Nginx y Cloudflare como capas de entrada;
* diagnóstico de incidencias reales en producción mediante logs y contenedores.

#### 🏗️ Infraestructura

```text
Usuario
   ↓
Cloudflare
   ↓
Edge Nginx
   ↓
Hetzner VPS
   │
   ├── Angular Store
   ├── Angular Admin
   ├── Laravel API
   ├── API Nginx
   ├── PostgreSQL
   ├── Redis
   ├── Queue Workers
   └── Scheduler
```

---

### 🛒 Camba  — Angular + Laravel
[Camba](https://www.camba.com.uy/)

> 🏗️ Arquitectura real • 🚀 Producción • 🧠 Decisiones técnicas • 📦 Fullstack

Proyecto **e-commerce real desarrollado para un cliente y actualmente en producción**, del cual armé una **versión sanitizada** para poder compartirlo públicamente como parte de mi portfolio.

Es, hasta el momento, **el proyecto más grande y complejo que desarrollé**, tanto por alcance funcional como por decisiones de arquitectura, performance y operación.

No es un proyecto académico ni una demo de features:  
la idea es mostrar **cómo se diseña, despliega y mantiene un sistema real en producción**.

#### 🔧 Stack y enfoque técnico

- **Frontend Store:** Angular 19 + SSR (SEO real y performance)
- **Frontend Admin:** Angular 16, completamente separado del store
- **Backend:** Laravel API REST sobre PHP-FPM
- **Redis:** cache distribuido, colas y rate limiting
- **Jobs y Scheduler:** procesamiento asíncrono y automatización
- **Docker:** entornos reproducibles (desarrollo y producción)
- **Infra:** Nginx + Cloudflare como capas de entrada y control
- **Deploy:** Hetzner VPS


#### 🎯 Problemas reales que resuelve

- Respuesta estable bajo carga
- SEO real incluso con filtros dinámicos
- Cacheo consciente con invalidación controlada
- Tareas pesadas fuera del request HTTP
- Separación clara de responsabilidades
- Infraestructura fácil de levantar, replicar y operar

🔗 

🎥 **Video demo (deep dive técnico)**  

📺 [YouTube – Demo técnica completa](https://www.youtube.com/watch?v=N1b5PfcdJiA)

📂 **Repositorio público (versión sanitizada)**  

🔗 [Repo Principal](https://github.com/GyabiSito/DemoEcommerceAngularLaravel)

🔗 [Api](https://github.com/GyabiSito/DemoEcommerceAngularLaravel-Api)

🔗 [Frontend](https://github.com/GyabiSito/DemoEcommerceAngularLaravel-Frontend)

🔗 [Admin](https://github.com/GyabiSito/DemoEcommerceAngularLaravel-Admin)


---

### 📅 ProConnect — Plataforma SaaS de Servicios Profesionales
[ProConnect](https://tallerphp.gyabisito.dev/)

> 🚀 SaaS multiusuario • 📅 Reservas y agenda • 💳 Pagos • ⚡ Tiempo real • 🎥 Videollamadas

**ProConnect** es una plataforma SaaS full stack desarrollada para gestionar de punta a punta la contratación de servicios profesionales.

El sistema conecta **clientes, profesionales y administradores** dentro de una misma plataforma, permitiendo gestionar servicios, disponibilidad, reservas, pagos, sesiones remotas, paquetes y reseñas.

El proyecto fue diseñado con una arquitectura desacoplada y desplegado en infraestructura real, cubriendo no solamente frontend y backend, sino también **concurrencia, tiempo real, integraciones externas, seguridad, Docker, CI/CD y operación en producción**.

#### 🔧 Stack y arquitectura

* **Frontend:** Angular + TypeScript + TailwindCSS
* **Backend:** Laravel 13 + API REST
* **Base de datos principal:** PostgreSQL
* **Redis:** cache, colas, locks y soporte para procesos asíncronos
* **Laravel Horizon:** procesamiento y monitoreo de jobs
* **MongoDB:** activity logs y auditoría
* **Laravel Reverb:** comunicación en tiempo real mediante WebSockets
* **LiveKit / WebRTC:** videollamadas integradas
* **MercadoPago:** pagos y confirmación mediante webhooks
* **OAuth:** Google y GitHub
* **Autenticación:** JWT, verificación de email y recuperación de contraseña
* **Docker:** servicios contenerizados y entornos reproducibles
* **Infraestructura:** Hetzner VPS + Nginx + Cloudflare
* **CI/CD:** GitHub Actions

#### 🎯 Funcionalidades principales

* 👤 Roles de **cliente, profesional y administrador**
* 🔎 Marketplace y búsqueda de servicios profesionales
* 🧑‍💼 Gestión de perfiles profesionales
* 🛠️ Creación y administración de servicios
* 🌐 Modalidades presencial, remota e híbrida
* 🗺️ Servicios asociados a ubicación geográfica
* 📅 Configuración avanzada de disponibilidad
* ⏱️ Generación automática de horarios reservables
* 🔒 Prevención de dobles reservas mediante transacciones y locking
* 🔄 Ciclo completo de estados de una reserva
* 💳 Integración con MercadoPago
* ⚡ Actualizaciones en tiempo real mediante WebSockets
* 🎥 Videollamadas asociadas a reservas mediante LiveKit
* 📦 Venta y gestión de paquetes de sesiones
* ⭐ Sistema de reseñas
* 🔔 Notificaciones
* 📊 Agenda profesional
* 🛡️ Policies, ownership y autorización desde backend
* 🧰 Panel administrativo
* 📝 Auditoría y activity logs

#### 🧠 Algunos desafíos técnicos

Uno de los principales desafíos fue diseñar correctamente el sistema de disponibilidad y reservas.

Los clientes **no pueden reservar horarios arbitrarios**. El sistema genera slots a partir de las reglas configuradas por cada profesional, teniendo en cuenta disponibilidad, duración del servicio, reservas existentes y diferentes restricciones.

Al momento de confirmar una reserva, el backend vuelve a validar el horario dentro de una operación transaccional y aplica mecanismos de locking para reducir condiciones de carrera y prevenir dobles reservas.

También se trabajó sobre:

* separación real entre frontend Angular y backend Laravel;
* autorización por roles y ownership de recursos;
* procesamiento de pagos basado en webhooks;
* sincronización de cambios en tiempo real;
* ejecución de tareas asíncronas mediante Redis y Horizon;
* integración de sesiones WebRTC;
* separación de auditoría respecto de los datos transaccionales;
* deployment de múltiples servicios Docker detrás de reverse proxies.

#### 🏗️ Infraestructura

```text
Usuario
   ↓
Cloudflare
   ↓
Edge Nginx
   ↓
Hetzner VPS
   │
   ├── Angular SPA
   ├── Laravel API
   ├── PostgreSQL
   ├── Redis
   ├── Horizon
   ├── Scheduler
   ├── MongoDB
   ├── Laravel Reverb
   └── LiveKit
```

🎥 **Video — Presentación técnica y funcional**

📺 *[Link](https://www.youtube.com/watch?v=b4GW1Y4OqFo)*

📂 **Código**

🔗 *[Repositorio](https://github.com/ProConnect-PHP/)*


## 🚀 Proyectos destacados

---

### ✈️ Sistema de Gestión de Aerolíneas – UTEC (2025)

> ✈️ Gestión de aerolíneas • 🧱 Clean Architecture • 🤝 Liderazgo técnico

Aplicación **completa** desarrollada por un equipo de 4 personas para administrar operaciones aéreas:

* 💻 Interfaz de escritorio con **Java Swing**
* 🌐 Backend con **JSP** y módulo **mobile**
* 🔗 Comunicación mediante **web services SOAP**
* 🔐 Autenticación y autorización usando **JWT**
* 🧠 Aplicación de **Clean Architecture**

🧑‍💼 Rol de **Líder Técnico**: brindé soporte y guía a los compañeros con menor experiencia en Java, asegurando calidad de código y buenas prácticas.


📂 **Código en GitHub**

🔧  [Rama Principal](https://github.com/volando-uy/volando-app)

🔧  [Servidor Central](https://github.com/volando-uy/app-central)

🔧  [Servidor Web](https://github.com/volando-uy/app-web)

🎥 **Video explicativo**

📺 [Video Demo](https://www.youtube.com/watch?v=4ouBXtXeoQg)

---

### 🛒 Proyecto E-commerce en PHP 8

> ✅ Fullstack • 🔐 Seguro • 🛠️ Modular • 🧠 Aprendizaje real

El año pasado desarrollé un sistema **E-commerce completo sin frameworks**, que recién ahora me animé a compartir.  
Fue un proyecto personal donde trabajé todo desde cero con:

- ⚙️ **PHP 8** (sin Laravel, sin frameworks)  
- 🛢️ **MariaDB / MySQL**  
- 🎨 **Bootstrap 5**, **JavaScript**, **jQuery**  
- 🔄 **AJAX + API interna**  
- 💳 Integración con **PayPal**, **MercadoPago** y **DLocal**  
- 🧾 Informes en PDF, favoritos, historial, ofertas, y mucho más  
- 🔐 Seguridad con `.htaccess`, tokens, protección de archivos sensibles

🎯 ¿Qué tiene?  
Carrito funcional, sistema de usuarios con verificación por email, variantes de productos, panel de administración, lógica de stock y validaciones para evitar inconsistencias.  
También apliqué principios de arquitectura limpia y separación de responsabilidades.


📂 **Código en GitHub**  
🔗 [Código](https://github.com/GyabiSito/ecommerce)

🎥 **Video explicando cómo lo hice**  
📺 [Video Demo](https://www.youtube.com/watch?v=coprFpWF-Co)

---

### 🎓 Proyecto de Tesis – UTU (2022)

> 🧩 Trabajo en equipo • 📚 Documentación completa • 🐧 Entorno Linux

Aplicación **full stack** desarrollada por un equipo de 5 personas con:

* ⚙️ **PHP**, **MySQL**, **HTML**, **CSS**, **JavaScript**
* 🗂️ Arquitectura basada en capas
* 🔄 Control de versiones con **Git/GitHub**
* 📈 Documentación: Pert, Gantt, análisis de requerimientos funcionales y no funcionales
* 💾 Base de datos en servidor **Linux**
* 🐚 Menú interactivo en **Shell Script** para facilitar la experiencia del usuario

🏆 Premiado como **Mejor Proyecto de Tesis 2022**


📂 **Código en GitHub**
🔧 *[...]*

🎥 **Video explicativo**
📺 *[...]*

---


### 🔧 [DesignPatterns](https://github.com/GyabiSito/DesignPatterns)
> Playground de **patrones de diseño** (GoF) implementados mayormente en **Java** y algunos en **C++**, con ejemplos prácticos y notas propias.

### 🧪 [Core-Java](https://github.com/GyabiSito/Core-Java)
> Ejercicios y mini-proyectos para dominar **Java Core**. Cubre desde sintaxis y POO hasta **colecciones**, **concurrencia**, **redes (sockets)** y **features de Java 8–18**.

### 🎓 [ATL-Academy](https://github.com/GyabiSito/ATLAcademy)
> Bootcamp intensivo de Backend Java con foco en Spring Boot, arquitectura limpia y testing profesional.

### 🧼 [SpringAFondo](https://github.com/GyabiSito/SpringAFondo)
> Guía práctica y progresiva de **Spring Framework** y **Spring Boot** con apuntes y ejemplos. Cubre desde IoC/DI y ciclo de vida de beans, hasta **Spring MVC**, **AOP**, **JDBC/ORM**, **Spring Data JPA**, **REST** y preparación para **entrevistas**.

### 🛠️ [LaravelCurso](https://github.com/GyabiSito/LaravelCurso)
> Laboratorio de **Laravel** con ejemplos modulares y prácticos: **auth (Breeze/Jetstream)**, **Blade**, **Eloquent/relaciones**, **CRUD/API**, **Eventos/Listeners**, **Mail**, **Storage**, **Localización**, **Testing**, **Livewire**, **Inertia**, **CSV/Excel**, **Asset Bundling & PDF**, **Middleware**

### 🤖 [AprendiendoSelenium](https://github.com/GyabiSito/AprendiendoSelenium)
> Guía práctica y modular para **automatizar pruebas web con Python + Selenium**: desde selectores y waits hasta **POM**, **DDT con Excel**, ejecución paralela y **BDD con behave**.

### 🅰️ [AprendiendoAngular](https://github.com/GyabiSito/AprendiendoAngular)
> Colección de proyectos prácticos en Angular que documentan un aprendizaje progresivo del framework: desde fundamentos y componentización, pasando por RxJS, state management (NGXS), routing y guards, consumo de APIs REST, formularios, Angular CDK (Drag & Drop, Virtual Scroll), performance frontend y patrones comunes usados en aplicaciones reales.
---

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GyabiSito&layout=compact&theme=radical)

---

## 📫 Conectemos

- LinkedIn: [José Gabriel Hernández](https://www.linkedin.com/in/jose-gabriel-hernandez-512899251/)

