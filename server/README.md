Dependencias

- typescript: Soporte hacia el lenguaje
- ts-node: Es la versión "node" para TS. Es para poder ejecutar "node index" pero en TS.

Para Ejecutar proyecto:
`npx ts-node src/index`

El npx es para ejecutarlo como si estuviera ts-node instalado de forma global
Si usamos nodemon entonces se reemplaza el npx por nodemon

_Configurar TS_

Cuando instalamos typescript tenemos acceso a un CLI propio de TS

Podemos ejecutar comando
`npx tsc src/index.ts`

Esto lo que hace es tomar el código de TS y lo convierte a una versión de JS, pero quedan todos revueltos dentro del mismo código.
Para arreglar esto debemos crear un archivo de configuración de TS en la raiz (tsconfig.json).

Definición del archivo:

```
{
  "compilerOptions": {
  "outDir": "./dist", --> Directorio donde se va a compilar el JS
  "rootDir": "./src", --> Directorio donde tenemos nuestro proyecto TS
  "lib": ["ESNext"], --> Versión de JS
  "strict": false, --> Strict en JS, se recomienda false por si no deja usar ñ
  "sourceMap": true,
  "esModuleInterop": true,
  "declaration": true
  }
}
```

Entonces ahora que ya tenemos el archivo tsconfig.js solo debemos ejecutar `npx tsc`
