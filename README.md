# Guía para Configurar y Usar Git y GitHub

## Creación y Configuración de Git y GitHub

### 1. Creación de una Cuenta en GitHub

Para comenzar, se debe crear una cuenta en GitHub desde la página oficial: [GitHub](https://github.com/).


### 2. Instalación de Git Bash

Descargar e instalar Git Bash desde el siguiente enlace: [Descargar Git](https://github.com/git-for-windows/git/releases/latest).

### 3. Configuración Inicial de Git

Ejecutar los siguientes comandos en Git Bash para configurar Git:


```sh
git config --global user.name "Tu Nombre de Usuario"
git config --global user.email "Email usado en la cuenta de GitHub"
git config --global init.defaultBranch main
git config --global color.ui auto
git config --global pull.rebase false
```

Para verificar la configuración:

```sh
git config --get user.name
git config --get user.email
```

### 4. Creación y Configuración de la Llave SSH

Generar una clave SSH con el siguiente comando (reemplazar con el email de GitHub):


```sh
ssh-keygen -t ed25519 -C "tuemail@email.com"
```

Presionar "Enter" hasta completar el proceso. Luego, copiar la clave SSH con:

```sh
cat ~/.ssh/id_ed25519.pub
```

Añadir la clave en GitHub desde: [Configuración de SSH en GitHub](https://github.com/settings/keys).

### 5. Prueba de la Conexión SSH

Ejecutar el siguiente comando para verificar la conexión:


```sh
ssh -T git@github.com
```

Si se muestra el mensaje de autenticación correcta, la conexión está lista.

## Clonación y Modificación de un Repositorio

### 1. Clonación de un Repositorio

Copiar el enlace SSH del repositorio desde GitHub y ejecutar:


```sh
git clone [enlace SSH]
```

### 2. Creación de Carpeta para el Repositorio

Ejecutar los siguientes comandos:

```sh
cd ~
mkdir repos
cd repos/
```

### 3. Verificación del Estado de los Archivos

Para revisar los cambios realizados:

```sh
git status
```

### 4. Agregar Archivos al Área de Envío

```sh
git add .
```

Verificar el estado nuevamente:

```sh
git status
```

### 5. Confirmar y Guardar Cambios en el Repositorio Local

```sh
git commit -m "Descripción del cambio realizado"
```

### 6. Ver Historial de Commits

```sh
git log
```

### 7. Envío de Cambios al Repositorio Remoto

```sh
git push origin main
```

### 8. Obtener Cambios de Otros Contribuidores

```sh
git pull origin main
```

## Conclusión

Siguiendo estos pasos, se puede configurar, clonar, modificar y sincronizar repositorios en GitHub de manera eficiente. Esta guía facilita el uso adecuado de Git y GitHub para la gestión de proyectos.
