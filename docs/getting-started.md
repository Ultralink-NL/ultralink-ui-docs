---
sidebar_position: 1
---

# Getting Started

Este archivo de documentación proporciona instrucciones detalladas sobre cómo instalar el paquete "Nombre del Paquete" en tu proyecto. El paquete ofrece componentes Vue reutilizables que te permiten crear tablas o listas con diferentes tipos de elementos de forma fácil y flexible.

### Requisitos Previos
Antes de instalar el paquete **"ultralink-ui"**, asegúrate de que tu proyecto cumpla con los siguientes requisitos previos:

### Node.js y npm 
Asegúrate de tener instalado Node.js y npm (Node Package Manager) en tu sistema. Puedes descargar e instalar la última versión de Node.js desde el sitio oficial: https://nodejs.org.

### Proyecto Vue 
Este paquete está diseñado para ser utilizado en proyectos Vue. Asegúrate de tener un proyecto Vue creado y configurado antes de continuar con la instalación del paquete.

### Instalación
Para instalar el paquete **"ultralink-ui"** en tu proyecto Vue, sigue los siguientes pasos:

Abre una terminal o línea de comandos en el directorio raíz de tu proyecto.

Ejecuta el siguiente comando para instalar el paquete **"ultralink-ui"** desde el registro de npm:

```bash title="Bash"
npm install ultralink-ui

```

### Uso
Una vez instalado el paquete "ultralink-ui" en tu proyecto, agrega los archivos css que necesitaras, de preferencia en la raiz del proyecto para que todo el proyecto tengo acceso a las variables de estilos.

```css title="App.vue"
import 'ultralink-ui/styles/ticketsColors.css'
import 'ultralink-ui/styles/brandColors.css'
import 'ultralink-ui/styles/labelColors.css'
```

### Listo

Con esto ya puedes utilizar los componentes reutilizables y puedes lograr construir interfaces con estos mismos.