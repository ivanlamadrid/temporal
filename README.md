# Upc202113432

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 19.2.10.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

## Running unit tests

To execute unit tests with the [Karma](https://karma-runner.github.io) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

# ───────────────────────────────
# 1. Creación de proyectos / workspaces
# ───────────────────────────────
ng new daos-1asi0729-learning-center
ng new daos-new-fakestore-products

# ───────────────────────────────
# 2. Angular Material
# ───────────────────────────────
cd daos-1asi0729-learning-center
ng add @angular/material
cd ../daos-new-fakestore-products
ng add @angular/material

# ───────────────────────────────
# 3. Librerías de internacionalización
# ───────────────────────────────
npm install @ngx-translate/core @ngx-translate/http-loader --save     # (en cada proyecto)

# ───────────────────────────────
# 4. JSON Server global
# ───────────────────────────────
npm install -g json-server@0.17.4

# ───────────────────────────────
# 5. Generación de entornos (Angular CLI ≥ 17)
# ───────────────────────────────
ng generate environments                           # (en ambos proyectos)

# ───────────────────────────────
# 6. Componentes, páginas y utilidades – Learning Center
# ───────────────────────────────
ng generate component learning/components/student-create-and-edit --skip-tests=true
ng generate component learning/pages/student-management --skip-tests=true
ng generate component public/components/language-switcher --skip-tests=true
ng generate component public/pages/about --skip-tests=true
ng generate component public/pages/home --skip-tests=true
ng generate component public/pages/page-not-found --skip-tests=true

ng generate class    learning/model/student             --type=entity    --skip-tests=true
ng generate service  shared/services/base               --skip-tests=true
ng generate service  learning/services/students         --skip-tests=true

# ───────────────────────────────
# 7. Componentes, modelos y servicios – Fake Store
# ───────────────────────────────
ng generate interface products/services/product response
ng generate class    products/model/rating              --type=entity    --skip-tests=true
ng generate class    products/model/product             --type=entity    --skip-tests=true
ng generate class    products/services/product          --type=assembler --skip-tests=true
ng generate service  products/services/fakestore-api    --skip-tests=true

ng generate component public/components/header-content   --skip-tests=true
ng generate component public/components/footer-content   --skip-tests=true
ng generate component public/components/language-switcher --skip-tests=true
ng generate component products/components/product-list   --skip-tests=true

# ───────────────────────────────
# 8. Módulo de eventos (registro + rating)
# ───────────────────────────────
# Modelos e interfaces
ng generate interface registration/services/event       response
ng generate interface registration/services/attendee    response
ng generate interface engagement/services/rating        response

ng generate class    registration/model/event           --type=entity    --skip-tests=true
ng generate class    registration/model/attendee        --type=entity    --skip-tests=true
ng generate class    engagement/model/rating            --type=entity    --skip-tests=true

# Assemblers
ng generate class    registration/services/event        --type=assembler --skip-tests=true
ng generate class    registration/services/attendee     --type=assembler --skip-tests=true
ng generate class    engagement/services/rating         --type=assembler --skip-tests=true

# Services (API)
ng generate service  registration/services/event-api    --skip-tests=true
ng generate service  registration/services/attendee-api --skip-tests=true
ng generate service  engagement/services/rating-api     --skip-tests=true

# Componentes
ng generate component registration/components/event-summary --skip-tests=true
# (Home standalone para mostrar el dashboard)
ng generate component public/pages/home                    --standalone --skip-tests=true

# ───────────────────────────────
# 9. Arranque de servidores locales
# ───────────────────────────────
# Angular dev-server
ng serve --port 4201

# JSON Server con rutas “/api/v1/*”
json-server --watch server/db.json --routes server/routes.json --port 3000

![image](https://github.com/user-attachments/assets/fc07786c-b983-4552-a461-583813d560ee)
