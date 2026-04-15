<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=timeGradient&height=250&section=header&text=GastroGram&fontSize=85&fontAlignY=35&animation=twinkling&desc=Donde%20el%20mundo%20se%20sienta%20a%20comer.&descAlignY=55&descSize=22" width="100%"/>

  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.herokuapp.com?font=Inter&weight=500&size=18&pause=1000&color=F7931E&center=true&vCenter=true&width=600&lines=El+proyecto+final+que+revoluciona+el+food-sharing;Comparte+recetas.+Conecta+con+foodies.;Arquitectura+moderna.+Diseño+pixel-perfect." alt="Typing SVG" />
  </a>

  <br />
  
  <a href="https://github.com/tu-usuario/gastrogram/stargazers">
    <img src="https://img.shields.io/github/stars/tu-usuario/gastrogram?style=for-the-badge&color=FFD700&labelColor=222222&logo=github" alt="Stars" />
  </a>
  <a href="https://github.com/tu-usuario/gastrogram/network/members">
    <img src="https://img.shields.io/github/forks/tu-usuario/gastrogram?style=for-the-badge&color=FF8C00&labelColor=222222&logo=git" alt="Forks" />
  </a>
  <a href="https://github.com/tu-usuario/gastrogram/issues">
    <img src="https://img.shields.io/github/issues/tu-usuario/gastrogram?style=for-the-badge&color=FF4500&labelColor=222222&logo=issuu" alt="Issues" />
  </a>
  <a href="https://gastrogram.app">
    <img src="https://img.shields.io/badge/Live_Demo-Online-10B981?style=for-the-badge&labelColor=222222&logo=vercel" alt="Demo Online" />
  </a>
</div>

<br />

> *"Comemos primero con los ojos. Y en el mundo digital, cocinamos con código."*

### 📖 La Visión detrás de GastroGram

Las aplicaciones de recetas tradicionales son aburridas y estáticas. Las redes sociales genéricas están llenas de ruido. **GastroGram nace para llenar ese vacío**. Desarrollado como un ambicioso proyecto final, GastroGram es una **red social de nicho** que combina la estética visual de Instagram con la utilidad práctica de un recetario profesional. 

No es solo código; es una plataforma pensada para creadores, diseñada para escalar y construida con las mejores prácticas de la industria actual.

---

<details open>
  <summary><b>📑 ÍNDICE DE CONTENIDOS (Clic para expandir)</b></summary>
  <br />
  
  1. [✨ Experiencia de Usuario (Features)](#-experiencia-de-usuario-features)
  2. [🛠️ Stack Tecnológico](#️-stack-tecnológico)
  3. [🏗️ Arquitectura de Software](#-arquitectura-de-software)
  4. [📂 Estructura del Ecosistema](#-estructura-del-ecosistema)
  5. [🚀 Instalación Rápida](#-instalación-rápida)
  6. [🔮 Visión a Futuro (Roadmap)](#-visión-a-futuro-roadmap)
  7. [👨‍💻 Los Arquitectos](#-los-arquitectos)

</details>

---

## ✨ Experiencia de Usuario (Features)

Para lograr un producto "Investor-Ready", nos enfocamos en una UI/UX impecable y funcionalidades que retienen al usuario.

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>📱 Scroll Infinito & Feed Dinámico</h3>
      <p>Un feed altamente adictivo impulsado por un algoritmo que prioriza el contenido visual. Soporta imágenes de alta resolución optimizadas al vuelo.</p>
      <ul>
        <li>Doble tap para "Me Gusta" (animación custom).</li>
        <li>Carga perezosa (Lazy Loading) de imágenes.</li>
        <li>Hilos de comentarios anidados.</li>
      </ul>
    </td>
    <td width="50%" align="center">
      <img src="https://cdn.dribbble.com/users/1615584/screenshots/15710288/media/6c8fbdeccb839849202eb89728cb1115.gif" width="250" style="border-radius: 15px;" alt="Feed Demo" />
    </td>
  </tr>
  <tr>
    <td width="50%" align="center">
      <img src="https://cdn.dribbble.com/users/2069402/screenshots/14470659/media/31a2ee7b2c58da4f4b259163e8a4a35e.gif" width="250" style="border-radius: 15px;" alt="Editor Demo" />
    </td>
    <td width="50%" valign="top">
      <h3>👨‍🍳 Creador de Recetas Inteligente</h3>
      <p>Publicar una receta debe ser tan satisfactorio como cocinarla. Nuestro editor paso a paso hace el trabajo pesado.</p>
      <ul>
        <li>Drag & Drop para imágenes.</li>
        <li>Auto-cálculo de tiempo total.</li>
        <li>Etiquetado de dietas (Keto, Vegano, Celiaco).</li>
      </ul>
    </td>
  </tr>
</table>

---

## 🛠️ Stack Tecnológico

Elegimos un stack moderno, fuertemente tipado y orientado al rendimiento. *(Iconos impulsados por skillicons.dev)*

<div align="center">
  <br />
  <p><b>Frontend Ecosystem</b></p>
  <img src="https://skillicons.dev/icons?i=ts,react,nextjs,tailwind,redux,framer&perline=10" alt="Frontend Stack" />
  
  <br /><br />
  
  <p><b>Backend & Data</b></p>
  <img src="https://skillicons.dev/icons?i=nodejs,express,postgres,prisma,redis,jwt&perline=10" alt="Backend Stack" />

  <br /><br />
  
  <p><b>Infraestructura & Tools</b></p>
  <img src="https://skillicons.dev/icons?i=docker,githubactions,vercel,aws,figma,postman&perline=10" alt="DevOps Stack" />
</div>

---

## 🏗️ Arquitectura de Software

El sistema utiliza un patrón **Monolito Modular** con vistas a una futura migración a microservicios. Separación estricta de responsabilidades (SoC).

```mermaid
graph TD;
    Client["Next.js Client (SSR/SSG)"]-->|REST / JSON| Gateway[Express API Gateway];
    Gateway-->Auth[Auth Service JWT];
    Gateway-->Feed[Feed & Recetas Service];
    Gateway-->Social[Interacciones & Seguidores];
    Feed-->Prisma[(PostgreSQL DB)];
    Social-->Prisma;
    Feed-->Cloudinary[Cloudinary CDN / Imágenes];
