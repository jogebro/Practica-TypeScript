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

