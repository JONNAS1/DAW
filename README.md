# DAW
DAW 2

# Introducción a GitHub y sus principales funciones

## Autor
**Nombre del autor:** [Joan Moliner Guinot]  
**Fecha:** [12/11/2025]  

---

## Introducción

**GitHub** es una plataforma en línea que permite **almacenar, gestionar y compartir código fuente** utilizando el sistema de control de versiones **Git**.  
Gracias a GitHub, desarrolladores de todo el mundo pueden **colaborar en proyectos**, hacer seguimiento de los cambios y trabajar de forma organizada y segura.

En este documento aprenderás a:
- Crear un repositorio en GitHub.  
- Añadir y subir archivos desde tu ordenador.  
- Crear y gestionar ramas (*branches*).
- Cambiar visibilidad de las ramas.  
- Realizar cambios y registrarlos con *commits*.  
- Crear *pull requests* y fusionar ramas.  
- Usar GitHub Pages para publicar un proyecto.  

El objetivo es comprender el funcionamiento básico de GitHub y adquirir una visión práctica de su uso.

---

## ⚙️ Pasos a seguir

### 1. Crear una cuenta en GitHub
1. Accede a [https://github.com](https://github.com).  
2. Haz clic en **Sign up** y completa el formulario con tu correo y contraseña.  
3. Confirma tu correo electrónico e inicia sesión.

---

### 2. Crear un nuevo repositorio
1. En la página principal, haz clic en **New repository**.  
2. Escribe un nombre para tu proyecto.  
3. Puedes añadir una breve descripción.  
4. Marca la opción **Add a README file** para crear este documento automáticamente.  
5. Haz clic en **Create repository**.

---

### 3. Añadir y subir archivos
**Opción 1 (desde la web):**  
- Haz clic en **Add file → Upload files** y selecciona los archivos desde tu ordenador.  
- Pulsa **Commit changes** para subirlos.  

**Opción 2 (con Git instalado):**  
```bash
git clone https://github.com/usuario/nombre-repositorio.git
cd nombre-repositorio
git add .
git commit -m "Añadir archivos iniciales"
git push origin main
