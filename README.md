<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=f7931e&height=280&section=header&text=Savorealo&fontSize=90&fontAlignY=38&animation=fadeIn&desc=Inteligencia%20Artificial%20al%20servicio%20de%20la%20gastronomía&descSize=20&descAlignY=60" width="100%" />

  <br />

  <a href="https://savorealo.com">
    <img src="https://img.shields.io/badge/PRODUCTION-SAVOREALO.COM-F7931E?style=for-the-badge&labelColor=1a1a1a" alt="Website" />
  </a>
  <img src="https://img.shields.io/badge/ANGULAR-v21-DD0031?style=for-the-badge&labelColor=1a1a1a&logo=angular" alt="Angular" />
  <img src="https://img.shields.io/badge/MOBILE-FLUTTER_%7C_KOTLIN-02569B?style=for-the-badge&labelColor=1a1a1a&logo=flutter" alt="Mobile Stack" />
  <img src="https://img.shields.io/badge/CI%2FCD-GITHUB_ACTIONS-2088FF?style=for-the-badge&labelColor=1a1a1a&logo=github-actions" alt="CI/CD" />
</div>

<br />

---

### Visión Ejecutiva

Savorealo redefine la interacción digital en el sector culinario. No es simplemente una red social, sino un ecosistema integral que combina **IA generativa**, análisis de datos avanzado y una arquitectura multiplataforma. El proyecto ha evolucionado de una estructura base a un sistema de alto rendimiento, destacando la migración crítica de Angular 19 a Angular 21 para aprovechar las últimas optimizaciones del framework.

---

### Índice de Arquitectura

1. [Innovación con IA](#innovación-con-ia)
2. [Ecosistema Tecnológico](#ecosistema-tecnológico)
3. [Estructura de Datos y Análisis](#estructura-de-datos-y-análisis)
4. [Infraestructura y Despliegue](#infraestructura-y-despliegue)
5. [Arquitectura de Microservicios](#arquitectura-de-microservicios)
6. [Repositorios del Proyecto](#repositorios-del-proyecto)

---

### Innovación con IA

El núcleo diferencial de Savorealo es su **Generador de Recetas con IA**, integrado mediante modelos de lenguaje avanzados (Claude).

* **Generación Contextual:** Creación de recetas basadas en ingredientes disponibles, restricciones dietéticas y preferencias culturales.
* **Optimización de Flujos:** Uso de **n8n** para la orquestación de flujos de trabajo inteligentes entre la IA y la base de datos.
* **Asistente Inteligente:** Implementación de procesamiento de lenguaje natural para guiar al usuario en tiempo real.

---

### Ecosistema Tecnológico

#### Frontend & Mobile
* **Core:** Angular 21 (Migración exitosa desde v19 para optimización de Signals y SSR).
* **Design System:** Tailwind CSS con componentes PrimeNG personalizados en la gama naranja/amarillo.
* **Mobile:** Desarrollo híbrido con Flutter (Dart) y módulos nativos en Kotlin.
* **Diseño UI/UX:** Prototipado de alta fidelidad en Figma.

#### Backend & Persistencia
* **API:** GraphQL para consultas eficientes y tipado estricto.
* **ORM:** Prisma para la gestión de modelos y migraciones.
* **BaaS:** Supabase (Auth, Realtime Database, Storage).
* **Lógica:** TypeScript como lenguaje unificado en todo el stack.

---

### Estructura de Datos y Análisis

Savorealo utiliza el dato como motor de crecimiento.

* **Procesamiento:** Uso de **Pandas** para la limpieza y estructuración de grandes volúmenes de datos culinarios.
* **Business Intelligence:** Dashboards en **Power BI** para el seguimiento de KPIs, tendencias de consumo y engagement de usuarios.

---

### Arquitectura de Microservicios

```mermaid
graph TD;
    User["Usuario (Web/Mobile)"] -->|GraphQL| Cloudflare["Cloudflare (WAF/CDN)"];
    Cloudflare --> Gateway["API Gateway (TypeScript)"];
    Gateway --> AI["Claude AI Engine / n8n"];
    Gateway --> DB["Supabase (PostgreSQL / Prisma)"];
    DB --> DataAnalysis["Pipeline de Datos (Pandas)"];
    DataAnalysis --> BI["Power BI Reports"];
    
    subgraph "CI/CD Pipeline"
    Github["GitHub Repository"] --> Actions["GitHub Actions"];
    Actions --> Deploy["Vercel / Cloudflare Pages"];
    end
