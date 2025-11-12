# Seguridad y Buenas Prácticas del Repositorio

Este documento describe las medidas de seguridad implementadas en el repositorio, la justificación para excluir ciertos archivos del control de versiones y las recomendaciones para proteger la integridad y confidencialidad del proyecto.

---

## 1. Archivos Excluidos del Control de Versiones

El archivo `.gitignore` evita que los siguientes archivos y directorios se suban al repositorio:

* .env, *.env.local: Contienen variables de entorno sensibles como contraseñas, tokens y claves API.
* node_modules/: Dependencias instaladas automáticamente, ocupan mucho espacio y son regenerables.
* dist/, `build/`: Archivos generados durante la compilación o construcción del proyecto.
* *.log: Archivos de registro que pueden contener información privada o ser voluminosos.
* *.tmp, *.swp: Archivos temporales o de intercambio de editores de texto.
* .idea/, .vscode/: Configuraciones específicas de IDEs/Editores.
* *.sqlite, *.db: Bases de datos locales que no deben compartirse.
* .DS_Store: Archivo de configuración de macOS, irrelevante para el proyecto.

---

## 2. Medidas de Seguridad Recomendadas

### Control de Acceso y Permisos

* **Ramas protegidas:** Las ramas principales (**main, master, develop**) deben estar protegidas para evitar pushes directos. Solo se permiten cambios mediante pull requests revisadas por al menos un colaborador.
* **Revisión de código:** Todo cambio debe ser revisado por otro miembro del equipo antes de ser fusionado.
* **Permisos por rol:** Los permisos en GitHub deben asignarse según el rol del colaborador (ver sección 4).

### Copias de Seguridad

* Utilizar la funcionalidad de "Branch Protection" y "Required Status Checks" en GitHub para evitar errores.
* Mantener clones actualizados del repositorio en máquinas seguras de los colaboradores.
* Configurar GitHub Actions para realizar backups automáticos o notificaciones de cambios críticos.

### Recuperación del Repositorio

En caso de pérdida de datos o errores graves, se garantiza la recuperación mediante:

* Restauración desde la papelera de GitHub o desde un fork.
* Clones locales actualizados en las máquinas de los colaboradores.
* Uso del historial de Git para volver a versiones anteriores del código mediante `git reset` o `git revert`.

---

## 3. Configuración de Permisos en GitHub

Los permisos en GitHub se asignan según el rol del colaborador en el equipo:

* **Desarrollador junior:** Permiso **Write**. Puede hacer push a ramas no protegidas y abrir pull requests.
* **Desarrollador senior:** Permiso **Write**. Puede revisar y fusionar pull requests, pero no gestionar configuraciones del repositorio.
* **Líder técnico:** Permiso **Admin**. Puede gestionar configuraciones, ramas protegidas y permisos de colaboradores.
* **Stakeholder externo:** Permiso **Read**. Solo puede visualizar el repositorio, sin capacidad de modificación.

---

## 4. Evidencias y Pruebas Realizadas

Se adjuntan capturas de pantalla y logs que demuestran:

* Configuración de permisos en GitHub.
* Pruebas de acceso según cada rol.
* Configuración de ramas protegidas.
* Ejemplos de pull requests y revisiones de código.

---
