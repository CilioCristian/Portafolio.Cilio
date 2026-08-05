# Portafolio.Cilio
## Clonar el proyecto
> **Importante:** No descargar el proyecto como ZIP. Siempre clonar el repositorio para conservar el historial de Git.
```bash
git clone https://github.com/CilioCristian/Portafolio.Cilio.git
```
Entrar a la carpeta:
```bash
cd Portafolio.Cilio
```
Verificar la rama:
```bash
git branch
```
Debe mostrar:
```text
* main
```
---
# Docker provee instrucciones dedicadas para cada sistema operativo.
# Por favor consulta la documentación oficial en https://www.docker.com/get-started/

# Descarga la imagen de Docker de Node.js:
docker pull node:24-alpine

# Crea un contenedor de Node.js e inicia una sesión shell:
docker run -it --rm --entrypoint sh node:24-alpine

# Verifica la versión de Node.js:
node -v # Debería mostrar "v24.19.0".

# Verifica versión de npm:
npm -v # Debería mostrar "11.17.0".

# Instalar dependencias
Instalar todas las dependencias del proyecto:
```bash
npm install
```
Esto generará automáticamente la carpeta `node_modules`.
---
# Ejecutar Sass
Si el proyecto utiliza el script configurado en `package.json`:
```bash
npm run sass
```
---
# Verificar el estado del repositorio
```bash
git status
```
Debe indicar:
```text
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
```
---
# Flujo de trabajo diario
Traer los últimos cambios antes de empezar:
```bash
git pull
```
---
Guardar los cambios realizados:
```bash
git add .
git commit -m "Descripción de los cambios"
git push
```
Ejemplo:
```bash
git add .
git commit -m "Agrego nueva sección de proyectos"
git push
```
---
# Estructura del proyecto
```text
Portafolio.Cilio/
│
├── src/
│   ├── css/
│   ├── images/
│   └── scss/
│
├── index.html
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```
---
# Buenas prácticas
* ✅ Clonar siempre el repositorio con `git clone`.
* ❌ No utilizar **Download ZIP**.
* ✅ Ejecutar `npm install` después de clonar el proyecto.
* ✅ Hacer `git pull` antes de comenzar a trabajar.
* ✅ Realizar `git push` cuando finalices tus cambios.
* ❌ No subir la carpeta `node_modules`.
* ❌ No modificar el archivo `.gitignore` sin necesidad.

/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Etapa 1 - HTML + SCSS (ahora)

El objetivo es dejar una réplica visual de Windows 11.

Nada de JavaScript todavía.

Vamos a construir todos los componentes:

 Escritorio✅
 Barra de tareas
 Menú Inicio
 Buscador
 Explorador
 Chrome
 Papelera
 Centro de notificaciones
 Calendario
 Animaciones CSS

Aunque no funcionen, tienen que verse igual que Windows.
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Etapa 2 - JavaScript

Una vez que todo esté maquetado:

Abrir y cerrar el menú Inicio.
Abrir el buscador.
Abrir ventanas.
Minimizar.
Maximizar.
Cerrar.
Arrastrar ventanas.
Actualizar el reloj.
Navegar entre secciones.

Ahí recién empezamos con la lógica.
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Etapa 3 - React

Acá haríamos una refactorización.

En vez de tener un HTML enorme, cada pieza pasa a ser un componente.

Por ejemplo:

src/
│
├── components/
│   ├── Taskbar/
│   ├── StartMenu/
│   ├── Search/
│   ├── Explorer/
│   ├── Chrome/
│   ├── Desktop/
│   ├── Clock/
│   └── NotificationCenter/
│
├── pages/
│
└── App.jsx

Y ahí React realmente aporta valor, porque vas a manejar el estado de las ventanas, qué está abierto, qué está minimizado, etc.
/////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
Etapa 4 - Backend (solo si hace falta)

Acá me haría una pregunta:

¿Qué necesita guardar este portfolio?

Si solo muestra información (Sobre mí, proyectos, contacto), no necesitás backend.

Pero si querés agregar cosas como:

Formulario de contacto.
Panel de administración para subir proyectos.
Base de datos con proyectos.
Sistema de autenticación.
Contador de visitas.
Blog.

Ahí sí tendría sentido.

Yo usaría algo como:

Node.js + Express.
PostgreSQL o MongoDB.
Prisma (si elegís SQL).
//////////////////////////////////////////////////////////////////////////////////////////
Un consejo que te va a servir mucho

A partir de ahora, cada vez que tengas que elegir entre vh y px, preguntate:

¿Estoy construyendo una página web adaptable o estoy copiando una interfaz específica?

🌍 Página web → rem, %, vh, vw.
🖥️ Interfaz tipo Windows → px en la mayoría de los casos.

Con esa regla vas a tomar decisiones mucho más fáciles.