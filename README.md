# VODWatch 🎬
> Plataforma de Video Bajo Demanda - Demo CI/CD Pipeline

[![Node.js](https://img.shields.io/badge/Node.js-18.x-green.svg)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-blue.svg)](https://expressjs.com/)
[![AWS](https://img.shields.io/badge/AWS-CodePipeline-orange.svg)](https://aws.amazon.com/codepipeline/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Una aplicación web de streaming tipo Netflix desarrollada para demostrar la implementación de un pipeline CI/CD completamente automatizado usando AWS CodePipeline y Elastic Beanstalk.

## 🚀 Demo en Vivo

- **Aplicación:** [URL de tu deployment]
- **Health Check:** [URL]/health
- **Pipeline:** AWS CodePipeline (privado)

## 📋 Características

### 🎥 Plataforma de Streaming
- **Interfaz moderna** tipo Netflix/Prime Video
- **Catálogo organizado** por categorías
- **Diseño responsive** para todos los dispositivos
- **Hover effects** e interacciones dinámicas
- **Dark theme** optimizado para streaming

### 🔄 CI/CD Automatizado
- **Deployment automático** en cada push a main
- **Pipeline de 2 etapas:** Source → Deploy
- **Health checks** integrados
- **Rollback automático** en caso de fallos
- **Tiempo de deployment:** 6-10 minutos

## 🏗️ Arquitectura

```
┌─────────────┐    ┌──────────────────┐    ┌─────────────────┐    ┌─────────────┐
│   GitHub    │───▶│  AWS CodePipeline │───▶│ Elastic Beanstalk │───▶│ EC2 Instance │
│ Repository  │    │    (Pipeline)     │    │   (PaaS Deploy)   │    │ (App Server) │
└─────────────┘    └──────────────────┘    └─────────────────┘    └─────────────┘
       │                       │                        │                    │
   git push              Webhook Trigger           Auto Deploy         Live Application
```

## 🛠️ Stack Tecnológico

### Frontend
- **HTML5** con estructura semántica
- **CSS3** con Flexbox y animaciones
- **JavaScript** vanilla para interacciones
- **Responsive Design** mobile-first

### Backend
- **Node.js** 18.x runtime
- **Express.js** web framework
- **Static file serving** para assets

### DevOps/Cloud
- **AWS Elastic Beanstalk** - Platform as a Service
- **AWS CodePipeline** - CI/CD orchestration  
- **GitHub Actions** - Source control integration
- **AWS CloudWatch** - Monitoring y logs

### Herramientas de Desarrollo
- **Git** para control de versiones
- **npm** para gestión de dependencias
- **VSCode** como IDE principal

## 📦 Instalación Local

### Prerrequisitos
- Node.js 18.x o superior
- npm o yarn
- Git

### Setup
```bash
# Clonar repositorio
git clone https://github.com/JpLetranger/VODWatch-app.git
cd VODWatch-app

# Instalar dependencias
npm install

# Ejecutar en desarrollo
npm start

# La aplicación estará disponible en http://localhost:3000
```

### Estructura del Proyecto
```
VODWatch-app/
├── README.md              # Este archivo
├── .gitignore            # Archivos ignorados por Git
├── package.json          # Configuración de npm y dependencias
├── package-lock.json     # Lock de versiones exactas
├── app.js               # Servidor Express principal
└── public/
    └── index.html       # Frontend de la aplicación
```

## 🚀 Deployment

### Pipeline Automatizado
El proyecto incluye un pipeline CI/CD completamente configurado:

1. **Push a GitHub** → Trigger automático
2. **Source Stage** → CodePipeline descarga código
3. **Deploy Stage** → Elastic Beanstalk despliega automáticamente
4. **Health Check** → Verificación de funcionamiento
5. **Go Live** → Aplicación disponible públicamente

### Deployment Manual (Alternativo)
```bash
# Para deployment manual en AWS Elastic Beanstalk
zip -r vodwatch-app.zip . -x "node_modules/*" ".git/*"
# Subir ZIP a Elastic Beanstalk console
```



## 🎯 Caso de Uso

Este proyecto fue desarrollado como demostración para:

### 📚 Evaluación Académica
- **Materia:** Infraestructura Cloud y DevOps
- **Objetivo:** Diseñar pipeline CI/CD para plataforma VOD
- **Alcance:** Automatización completa de deployment

### 💼 Skills Demostrados
- **Cloud Architecture** con AWS
- **DevOps Pipeline** automation
- **Full-stack Development** con Node.js
- **Infrastructure as Code** concepts
- **Modern UI/UX** design principles

## 🔐 Seguridad

### AWS IAM Roles Configurados
- **CodePipeline Service Role** con permisos específicos
- **Elastic Beanstalk Instance Profile** securizado
- **GitHub Integration** via AWS CodeStar Connections

### Best Practices Implementadas
- **Least privilege principle** en permisos IAM
- **Secrets management** via environment variables
- **HTTPS enforcement** en producción
- **Input validation** en endpoints públicos

## 📈 Monitoreo y Métricas

### CloudWatch Integration
- **Application logs** centralizados
- **Performance metrics** automáticas
- **Error tracking** y alertas
- **Uptime monitoring** 24/7

### Key Performance Indicators
- **Response Time:** < 200ms promedio
- **Uptime:** 99.9% target
- **Deployment Time:** 6-10 minutos
- **Error Rate:** < 0.1%



## 👨‍💻 Contribución

Este es un proyecto de demostración académica. Para sugerencias o mejoras:

1. **Fork** el repositorio
2. **Create feature branch:** `git checkout -b feature/nueva-funcionalidad`
3. **Commit changes:** `git commit -am 'Add nueva funcionalidad'`
4. **Push to branch:** `git push origin feature/nueva-funcionalidad`
5. **Submit Pull Request**

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver [LICENSE](LICENSE) para detalles.

## 📞 Contacto

**Desarrollador:** [Juan Pablo Gajardo]  
**Email:** [jgajardodev@gmail.com]  
**LinkedIn:** [(https://www.linkedin.com/in/juanpgajardo/)]  
**GitHub:** [@JpLetranger](https://github.com/JpLetranger)

---

### 🏆 Tecnologías y Herramientas

<div align="center">
  
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/-Express-000000?style=flat-square&logo=express&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

</div>

---

<div align="center">
  <p><strong>Desarrollado para Evaluación final Módulo 6 Bootcamp DevOps - ADALID = Talento Digital para Chile</strong></p>
  <p>© 2025 VODWatch Demo Project</p>
</div>