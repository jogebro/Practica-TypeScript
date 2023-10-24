# README - Guia de TypeScript

## Instalación de TypeScript
Ejecutar este comando en la terminal para la instalación:

```shell
npm install -g typescript
```

Verificar la instalación de TypeScript ejecutando:

```shell
tsc -v 
```

!Con esto ya estaria instalado TypeScript en el sistema!

## Transpilación
Para transpilar archivos se realiza el siguiente comando:

```shell
tsc index.ts 
```

Para transpilar el codigo en una carpeta especifica usamos:

```shell
tsc --outDir dist index.ts 
```

- **--outDir**: Este comando se utiliza para especificar la carpeta de salida.
- **dist**: Es el nombre de la carpeta donde deseas guardar los archivos transpilados.

Si queremos que el codigo se transpile automaticamente con cada cambio podemos usar:

```shell
tsc index.ts --w 
```

 Ó

```shell
tsc --outDir dist index.ts --w  
```

- **--w, --watch**: Se utiliza para que se observen los cambios que se realicen en el archivo y se transpilen.

## Ejecución
Para ejecutar el codigo ya transpilado se usa este comando:

```shell
node index.js 
```

Si el archivo esta en una carpeta se hace la ruta de esta forma:

```shell
node dist/index.js
```

## TsConfig
### Agregar al proyecto
Para agregar el tsconfig usamos el siguiente comando:

```shell
tsc --init
```

- **--init**: Con esto podemos agregar el tsconfig que nos ayudara a montar y configurar nuestro proyecto

### Configuración

#### outDir:

En el apartado de "Emit" podemos encontrar algo llamado **outDir: "./"**; Descomenta esta opcion y puedes hacer lo siguiente:

```
outDir: "./dist"
```

Con esto espeficicamos a que directorio queremos que automaticamente se guarden los archivos transpilados

#### rootDir:
En el apartado de "Modules" podemos encontrar algo llamado **rootDir: "./"**; Descomenta esta opcion y puedes hacer lo siguiente:

```
rootDir: "./src"
```

Con esto especificamos desde que carpeta nosotros queremos transpilar nuestros archivos

---
#### NOTA:
Una vez configurado esto ya no es necesario especificar donde queremos guardar los archivos, asi que se usa el comando normal:

```shell
tsc
```

Tambien puedes usar el -w:

```shell
tsc -w
```
---

#### target:
En el apartado de "Language and Environment" podemos encontrar algo llamado **"target"**; Esta propiedad define a que version se compila el codigo, esta version puede modificarse según lo requerido, se puede usar esta si se desea:

```
target: "ES6"
```


## Ayuda

En caso de necesitar más información puedes usar este comando:

```shell
tsc --help
```

