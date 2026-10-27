# 💰 Control de Cuchumbal

Sistema web para llevar el control de un cuchumbal (ahorro rotativo entre compañeros de trabajo).

## Funciones
- Acceso con usuario y contraseña (3 usuarios autorizados).
- Registro de participantes (nombre y apellido), mínimo 25, hasta 50.
- Cuota fija de L 300 semanales, 4 semanas por mes, 4 meses (16 semanas, total L 4,800 por persona).
- Búsqueda por nombre: al agregar otra cuota se suma a la misma persona, sin duplicar registros.
- Control semanal de pagos con "Lleva aportado" y "Falta" automáticos.
- Al llegar a L 4,800 no se aceptan más cuotas.
- Ruleta de turnos sin repetir; el turno sorteado se refleja en la tabla principal.
- Eliminar o anular registros requiere autorización del usuario administrador.

## Estructura
```
index.html        Estructura de la página
src/main.js       Lógica del sistema
src/style.css     Estilos
vite.config.js    Configuración de Vite
netlify.toml      Configuración de Netlify
dist-listo/       Versión ya lista para arrastrar a Netlify (sin compilar)
```

## Subir a Netlify

### Opción A: arrastrar y soltar (la más fácil, sin instalar nada)
1. Entra a https://app.netlify.com/drop
2. Arrastra la carpeta **dist-listo** (la que contiene `index.html`).
3. Netlify te da un enlace público.

### Opción B: desde GitHub (se compila solo)
1. Sube todo el contenido de esta carpeta a un repositorio de GitHub.
2. En Netlify: Add new site → Import an existing project → elige el repositorio.
3. Netlify lee `netlify.toml` (comando `npm run build`, carpeta `dist`). Pulsa Deploy.

### Opción C: compilar en tu computadora
```
npm install
npm run build
```
Luego arrastra la carpeta `dist` generada a Netlify.

## Desarrollo local
```
npm install
npm run dev
```

## Notas
- Los datos se guardan en el navegador (localStorage) del dispositivo donde se use.
- El login es una barrera de acceso en el navegador; no reemplaza un servidor con seguridad real.

Créditos: DENIS MAIRENA
