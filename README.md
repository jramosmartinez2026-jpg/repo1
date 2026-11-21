# NexoCatálogo

NexoCatálogo es una landing page responsive presentada como una propuesta visual para la gestión y organización de catálogos de productos. La interfaz reúne una presentación principal, beneficios, una sección de gestión y navegación interna, permitiendo consultar la información de forma clara y sencilla.

> Este proyecto está construido como una aplicación Angular. Aunque el nombre del paquete hace referencia a Firestore, el código incluido actualmente no contiene integración con Firebase ni persistencia de datos.

## Propósito

El objetivo de NexoCatálogo es mostrar una experiencia de usuario clara para:

- Presentar el catálogo y sus principales ventajas.
- Reunir y comunicar la información de los productos.
- Facilitar la navegación entre beneficios y áreas de gestión.
- Mantener una experiencia adaptable a equipos de escritorio y dispositivos móviles.
- Ofrecer accesibilidad básica mediante enlaces de salto, navegación semántica y estilos para elementos enfocados.

## Funciones principales

- **Hero informativo:** presenta el propósito del catálogo y enlaces de acción.
- **Beneficios:** muestra organización, claridad de gestión y control.
- **Vista de gestión:** incluye una sección introductoria para administrar el catálogo.
- **Navegación interna:** permite desplazarse entre inicio, beneficios y gestión.
- **Diseño responsive:** adapta el encabezado, columnas, tarjetas y pie de página a distintos tamaños de pantalla.
- **Accesibilidad:** incorpora un enlace «Saltar al contenido principal», etiquetas ARIA y estilos visibles para el foco del teclado.
- **Preferencia de movimiento reducido:** desactiva el movimiento principal mediante `prefers-reduced-motion`.

## Tecnologías utilizadas

- Angular 22
- Angular CLI
- TypeScript 6
- HTML
- CSS
- RxJS 7
- Vitest 4
- jsdom
- Prettier
- npm

La aplicación utiliza componentes independientes de Angular y configuración mediante `src/app/app.config.ts`. Los estilos principales están definidos en `src/app/app.css` y `src/styles.css`.

## Requisitos

- Node.js compatible con Angular 22 y el paquete especificado en el proyecto.
- npm 11.19.0 o compatible.
- Angular CLI 22.
- Navegador web moderno.

## Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/jramosmartinez2026-jpg/repo1.git
cd repo1
```

2. Instala las dependencias:

```bash
npm install
```

3. Opcionalmente, instala Angular CLI de forma global:

```bash
npm install -g @angular/cli
```

## Ejecución en desarrollo

Inicia el servidor de desarrollo con npm:

```bash
npm start
```

También puedes usar Angular CLI directamente:

```bash
ng serve
```

Abre `http://localhost:4200/` en el navegador. Angular recargará automáticamente la aplicación al modificar los archivos fuente.

## Configuración

El proyecto no requiere actualmente variables de entorno ni archivos de configuración externos.

- `angular.json` define la aplicación `catalogo-firestore`, los recursos públicos y las configuraciones de desarrollo y producción.
- `src/main.ts` inicia la aplicación Angular.
- `src/app/app.ts` contiene el componente principal.
- `src/app/app.html` contiene la estructura de la página.
- `src/app/app.css` contiene la mayoría de los estilos visuales y las reglas responsive.
- `src/styles.css` contiene los estilos globales.
- `public/` contiene los recursos estáticos que serán copiados a la compilación.

Si en el futuro se incorpora Firebase o Firestore, deberán añadirse las credenciales del proyecto y variables de configuración correspondientes sin almacenar secretos en el código fuente.

## Construcción para producción

Genera los archivos optimizados con:

```bash
npm run build
```

Los artefactos se guardarán en el directorio `dist/`. La configuración de producción incluye ofuscación de nombres, optimización y límites de tamaño establecidos en `angular.json`.

## Pruebas

Ejecuta las pruebas unitarias con Vitest mediante Angular CLI:

```bash
npm test
```

Las pruebas se encuentran actualmente en `src/app/app.spec.ts` y pueden ampliarse para comprobar el componente principal y nuevas funcionalidades.

## Formato de código

El proyecto incluye configuración de Prettier en `.prettierrc` y configuración del editor en `.editorconfig`. Puedes formatear manualmente los archivos desde tu editor o ejecutando Prettier mediante el CLI instalado como dependencia:

```bash
npx prettier --write .
```

## Estructura del proyecto

```text
repo1/
├── public/                 # Recursos públicos estáticos
├── src/
│   ├── app/
│   │   ├── app.ts          # Componente principal
│   │   ├── app.html        # Plantilla de la página
│   │   ├── app.css         # Estilos del componente
│   │   ├── app.config.ts   # Configuración de Angular
│   │   └── app.spec.ts     # Pruebas del componente
│   ├── index.html          # Documento HTML principal
│   ├── main.ts             # Punto de entrada
│   └── styles.css          # Estilos globales
├── angular.json            # Configuración de Angular CLI
├── package.json            # Dependencias y scripts npm
└── tsconfig.json           # Configuración de TypeScript
```
