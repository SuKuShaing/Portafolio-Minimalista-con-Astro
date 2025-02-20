# Portafolio Minimalista con Astro

Siguiendo el tutorial de Midudev en [Youtube](https://youtu.be/Zwh92LTB-Bk?si=YyTW_z6K4eiSUP3l)


## Configuración de tsconfig.json para importar módulos con alias (@)
```json
"compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "@/*": ["src/*"]
    }
  }
```

## Schema del JSON de CV, standar en:
https://jsonresume.org/schema


## Menú desplegable
usamos uno de los menú listados aquí:
https://github.com/stefanjudis/awesome-command-palette


### Menú desplegable Ninja-keys
El menú desplegable que usamos es Ninja-keys, se puede ver en:
https://github.com/ssleptsov/ninja-keys















## EPERM: operation not permitted, rmdir
Con esto se solucionan el error
```sh
$ npm run build

> generador-de-sitios-estaticos---fazt@0.0.1 build
> astro build

13:22:14 [types] Generated 1ms
13:22:14 [vite] Re-optimizing dependencies because lockfile has changed
EPERM: operation not permitted, rmdir 'D:\Progra\Platzi\Cursos Webs\Astro-Desarrollo-web\node_modules\.vite\deps'
  Stack trace:

```

ejecutando los 5 pasos de aquí, se soluciona (ojo comandos para consola windows, no funcionan en bash porque emula comandos Linux)

1. clean npm cache
```sh
npm cache clean --force
```

2. (Windows) delete node_modules and package-lock.json

```sh
rd /s /q "node_modules"
del package-lock.json
del -f yarn.lock
```

3. update your npm version
```sh
npm install -g npm@latest --force
```

4. clean npm cache
```sh
npm cache clean --force
```

5. install packages
```sh
npm install
```
