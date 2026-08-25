# 👋 Hi! I'm José Gabriel Hernández (GyabiSito)

📍 Uruguay | 💻 Full Stack Developer

I'm a software developer who enjoys understanding how systems work end-to-end — from frontend and backend development to databases, infrastructure, deployments, and production debugging.

I mainly work with **Angular, Java, Laravel, Spring, PostgreSQL, Redis, Docker, and Linux**, building projects that go beyond isolated features and cover complete application workflows.

---

## 🛠️ Technologies

![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=flat-square&logo=spring&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-E74430?style=flat-square&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=flat-square&logo=selenium&logoColor=white)

---

# 🚀 Featured Projects

## 🌿 Komorebi — Production E-commerce Platform

> 🛒 Real client • 💳 MercadoPago • ⚡ Redis & Queues • 🐳 Docker • 🚀 Production

🔗 [Live Website](https://komorebi.com.uy/)

**Komorebi** is a full-stack e-commerce platform developed for a real client and currently running in production.

The application is divided into three main components:

- Public Angular storefront
- Independent Angular administration panel
- Laravel REST API

It covers the complete online-store workflow, including product discovery, authentication, shopping cart, checkout, payments, inventory, order management, administration, transactional emails, and infrastructure.

### 🔧 Tech Stack

- **Store:** Angular
- **Admin Panel:** Angular
- **Backend:** Laravel REST API
- **Database:** PostgreSQL
- **Cache & Queues:** Redis
- **Payments:** MercadoPago
- **Email:** SMTP2GO
- **Infrastructure:** Docker, Nginx, Hetzner VPS, Cloudflare

### 🎯 Key Features

- Product catalog and filtering
- User registration and authentication
- Shopping cart
- MercadoPago checkout
- Payment confirmation through webhooks
- Order lifecycle management
- Product and inventory administration
- Administrative metrics
- Transactional and administrative emails
- Asynchronous processing with Redis queues
- Scheduled background tasks
- Containerized production deployment

### 🧠 Technical Highlights

Payment confirmation is handled by the backend using **MercadoPago webhooks**, rather than relying exclusively on browser redirects.

This allows the application to reliably update orders and inventory even when the customer closes the browser or the checkout redirect never reaches the frontend.

The project also involved production troubleshooting through Docker logs, reverse proxy configuration, authentication between separate applications, queue workers, scheduled jobs, and infrastructure management.

---

## 🛒 Camba — Production Angular + Laravel E-commerce

> 🏗️ Real architecture • 🚀 Production • 🧠 Technical decisions • 📦 Full Stack

🔗 [Live Website](https://www.camba.com.uy/)

**Camba** is a real e-commerce platform developed for a client and currently running in production.

Because the original project contains private client information, I created a **sanitized public version** that demonstrates its architecture and implementation without exposing sensitive data.

It is one of the largest projects I have worked on in terms of functionality, architecture, performance, and infrastructure.

### 🔧 Tech Stack

- **Store:** Angular 19 + SSR
- **Admin Panel:** Angular 16
- **Backend:** Laravel REST API
- **Runtime:** PHP-FPM
- **Cache:** Redis
- **Queues & Scheduled Jobs**
- **Docker**
- **Nginx**
- **Cloudflare**
- **Hetzner VPS**

### 🎯 Engineering Focus

- Server-side rendering for SEO
- Dynamic filtering with SEO support
- Distributed caching
- Controlled cache invalidation
- Background processing outside HTTP requests
- Rate limiting
- Separation between Store, Admin, and API
- Reproducible Docker environments
- Production deployment and maintenance

🎥 **Technical walkthrough — Spanish audio**

📺 [YouTube – Full Technical Demo](https://www.youtube.com/watch?v=N1b5PfcdJiA)

### 📂 Public Sanitized Version

- [Main Repository](https://github.com/GyabiSito/DemoEcommerceAngularLaravel)
- [Backend API](https://github.com/GyabiSito/DemoEcommerceAngularLaravel-Api)
- [Frontend Store](https://github.com/GyabiSito/DemoEcommerceAngularLaravel-Frontend)
- [Admin Panel](https://github.com/GyabiSito/DemoEcommerceAngularLaravel-Admin)

---

## 📅 ProConnect — Professional Services SaaS Platform

> 🚀 Multi-user SaaS • 📅 Booking System • 💳 Payments • ⚡ Real-time • 🎥 Video Calls

🔗 [Live Application](https://tallerphp.gyabisito.dev/)

**ProConnect** is a full-stack SaaS platform designed to manage the complete lifecycle of hiring professional services.

It connects **clients, professionals, and administrators** in the same ecosystem and supports services, availability, reservations, payments, remote sessions, packages, reviews, and administration.

### 🔧 Tech Stack

- **Frontend:** Angular + TypeScript + TailwindCSS
- **Backend:** Laravel 13 REST API
- **Database:** PostgreSQL
- **Cache & Queues:** Redis
- **Queue Monitoring:** Laravel Horizon
- **Audit Logs:** MongoDB
- **WebSockets:** Laravel Reverb
- **Video Calls:** LiveKit / WebRTC
- **Payments:** MercadoPago
- **OAuth:** Google & GitHub
- **Authentication:** JWT
- **Infrastructure:** Docker, Nginx, Hetzner VPS, Cloudflare
- **CI/CD:** GitHub Actions

### 🎯 Key Features

- Client, professional, and administrator roles
- Professional services marketplace
- Professional profiles
- Service management
- On-site, remote, and hybrid services
- Advanced availability configuration
- Automatic bookable slot generation
- Booking lifecycle management
- Double-booking prevention
- MercadoPago payments
- Real-time updates through WebSockets
- Integrated video calls
- Session packages
- Reviews and ratings
- Notifications
- Professional calendar
- Administrative dashboard
- Activity logs and auditing

### 🧠 Technical Highlights

One of the most important challenges was designing the **availability and booking system**.

Users cannot reserve arbitrary times. Available slots are generated from rules configured by each professional while considering service duration, existing reservations, availability constraints, and scheduling rules.

During confirmation, the backend validates availability again inside a database transaction and applies locking mechanisms to reduce race conditions and prevent double bookings.

🎥 **Technical & Functional Walkthrough — Spanish audio**

📺 [YouTube Demo](https://www.youtube.com/watch?v=b4GW1Y4OqFo)

📂 [Source Code](https://github.com/ProConnect-PHP/)

---

## ⚡ Voltio — EV Charging Platform

> ⚡ Electric Vehicles • 🗺️ Interactive Maps • 📅 Reservations • 🛣️ Route Planning • 🐳 Docker

🔗 [Live Application](https://voltio.gyabisito.dev/)

**Voltio** is a full-stack platform for discovering, sharing, and booking electric vehicle charging points.

The platform connects **Drivers and Hosts**, allowing charging infrastructure to be discovered and managed through an interactive map while supporting reservations, availability, reviews, vehicles, and route planning.

### 🔧 Tech Stack

- **Frontend:** Angular
- **Backend:** Laravel REST API
- **Database:** PostgreSQL
- **Geospatial Data:** PostGIS
- **Cache & Background Processing:** Redis
- **Real-time Communication:** Laravel Reverb
- **Maps & Routing:** Mapbox
- **Docker**
- **Nginx**
- **Cloudflare**
- **Hetzner VPS**

### 🎯 Key Features

- Interactive charging-point map
- Charging station discovery and filtering
- Driver and Host roles
- Charging-point management
- Reservation workflows
- Availability management
- User vehicles
- Charging sessions
- Reviews
- Popular EV routes
- Route-based charger discovery
- Energy-aware route planning
- Administrative interface
- Real-time features

### 🧠 Technical Highlights

Voltio combines traditional application data with **geospatial search and route planning**.

The platform works with map viewports, geographic coordinates, charging-point filters, external routing data, and route geometry to identify relevant charging locations along a journey.

The complete platform is containerized and deployed behind a shared production reverse-proxy infrastructure.

---

## ✈️ VolandoUY — Airline Management System

> ✈️ Airline Operations • 🧱 Clean Architecture • 🔐 JWT • 🤝 Technical Leadership

Full airline management system developed by a **4-person team at UTEC**.

The system combines desktop, web, and mobile components communicating through web services.

### 🔧 Tech Stack

- **Desktop:** Java Swing
- **Web:** JSP
- **Web Services:** SOAP
- **Authentication:** JWT
- **Architecture:** Clean Architecture
- **Additional mobile module**

### 👨‍💻 My Role

I worked as **Technical Lead**, supporting team members with less Java experience, helping define implementation approaches, reviewing technical decisions, and promoting maintainable code.

### 📂 Source Code

- [Main Repository](https://github.com/volando-uy/volando-app)
- [Central Server](https://github.com/volando-uy/app-central)
- [Web Server](https://github.com/volando-uy/app-web)

🎥 **Project Walkthrough — Spanish audio**

📺 [YouTube Demo](https://www.youtube.com/watch?v=4ouBXtXeoQg)

---

## 🛒 E-commerce Platform — PHP 8 From Scratch

> ✅ Full Stack • 🔐 Security • 🛠️ Modular Architecture • PHP Without Frameworks

A complete e-commerce system developed in **PHP 8 without Laravel or another backend framework**.

The project was built to understand and implement many of the mechanisms normally abstracted by modern frameworks.

### 🔧 Tech Stack

- PHP 8
- MariaDB / MySQL
- Bootstrap 5
- JavaScript
- jQuery
- AJAX
- Internal APIs

### 🎯 Key Features

- Product catalog
- Shopping cart
- User authentication
- Email verification
- Product variants
- Inventory management
- Administration panel
- Favorites
- Purchase history
- Discounts and promotions
- PDF reports
- PayPal integration
- MercadoPago integration
- DLocal integration
- Security controls using tokens and `.htaccess`

The project also applies separation of responsibilities and architectural principles without relying on a full-stack framework.

📂 [Source Code](https://github.com/GyabiSito/ecommerce)

🎥 **Technical Walkthrough — Spanish audio**

📺 [YouTube Demo](https://www.youtube.com/watch?v=coprFpWF-Co)

---

# 📚 Other Projects

## 🎓 UTU Thesis Project — 2022

> 🏆 Best Thesis Project 2022 • 🧩 Teamwork • 📚 Documentation • 🐧 Linux

Full-stack application developed by a team of five students.

### Technologies

- PHP
- MySQL
- HTML
- CSS
- JavaScript
- Git / GitHub
- Linux
- Shell scripting

The project included technical and project documentation such as:

- Functional requirements
- Non-functional requirements
- PERT planning
- Gantt charts
- Database design
- Layered architecture

A Shell Script-based interactive menu was also created to simplify system operation.

🏆 **Awarded Best Thesis Project 2022**

---

## 🔧 [DesignPatterns](https://github.com/GyabiSito/DesignPatterns)

A playground for studying and implementing **Gang of Four design patterns**, primarily in Java with additional C++ examples.

---

## ☕ [Core-Java](https://github.com/GyabiSito/Core-Java)

Exercises and mini-projects focused on mastering Java fundamentals.

Topics include:

- Object-Oriented Programming
- Collections
- Concurrency
- Networking and sockets
- Java 8–18 features

---

## 🎓 [ATL-Academy](https://github.com/GyabiSito/ATLAcademy)

Backend Java bootcamp focused on **Spring Boot, clean architecture, and professional testing practices**.

---

## 🧼 [SpringAFondo](https://github.com/GyabiSito/SpringAFondo)

A practical and progressive guide to **Spring Framework and Spring Boot**.

Topics include:

- IoC / Dependency Injection
- Bean lifecycle
- Spring MVC
- AOP
- JDBC / ORM
- Spring Data JPA
- REST APIs
- Interview preparation

---

## 🛠️ [LaravelCurso](https://github.com/GyabiSito/LaravelCurso)

Laravel learning laboratory containing modular examples covering:

- Authentication with Breeze and Jetstream
- Blade
- Eloquent and relationships
- CRUD and REST APIs
- Events and listeners
- Mail
- Storage
- Localization
- Testing
- Livewire
- Inertia
- CSV / Excel
- Asset bundling
- PDF generation
- Middleware

---

## 🤖 [AprendiendoSelenium](https://github.com/GyabiSito/AprendiendoSelenium)

Practical repository for learning **web test automation with Python and Selenium**.

Topics include:

- Selectors
- Explicit waits
- Page Object Model
- Data-Driven Testing with Excel
- Parallel execution
- BDD with Behave

---

## 🅰️ [AprendiendoAngular](https://github.com/GyabiSito/AprendiendoAngular)

Collection of practical Angular projects documenting a progressive learning path through the framework.

Topics include:

- Components
- RxJS
- State management with NGXS
- Routing
- Guards
- REST APIs
- Reactive forms
- Angular CDK
- Drag & Drop
- Virtual Scroll
- Frontend performance
- Common application patterns

---

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=GyabiSito&layout=compact&theme=radical)

---

# 📫 Let's Connect

- [LinkedIn — José Gabriel Hernández](https://www.linkedin.com/in/jose-gabriel-hernandez-512899251/)
