---
title: "✍️ Creando nuestro sitio web"
date: 2018-03-03T19:06:03+01:00
draft: false
tags: ["create"]
categories: ["Workshop"]
---

## Creando nuestro sitio web


Ahora que tenemos Hugo instalado, el siguiente paso es crear nuestro sitio web. Lo haremos con el siguiente comando:
```
hugo new site web2  
```
<!--more-->
Donde `web2` se corresponde con el nombre que yo he querido darle a mi nuevo sitio web. Puedes ponerle el nombre que quieras.  

Una vez hecho esto, accedemos a la carpeta desde la terminal:
```
cd web2
```

Si hacemos un `ls` para ver lo que ha generado Hugo, deberíamos tener un listado de ficheros como este:
![Listado-ficheros](/img/03/file-list.png)

Podemos ver que tenemos varias carpeta vacías, y que solo tenemos 2 archivos: `archetypes/default.md` y `config.toml`.  
No te asustes si no reconoces los formatos de los ficheros.

Más adelante vamos a explicar para qué sirve cada carpeta y como ir dándole forma a nuestro sitio web.
Y verás que es super fácil crear sitios web con Hugo.

Vamos a dejar esto de lado temporalmente y vamos ver que aspecto tendría nuestra web.

## Instalando un tema
Tema, plantilla, template, theme.. lo puedes llamar como quieras. Antes de poder hacer nada, necesitamos instalar un tema para
nuestra web. Puedes ver el listado de temas disponibles para Hugo [aquí](https://themes.gohugo.io/).

Aunque todos los temas comparten bastante en cuanto a su forma de uso, hay diferencias entre unos y otros.
Para evitar confusiones, vamos a instalar el tema [Even](https://themes.gohugo.io/hugo-theme-even/).

Para instalarlo, desde la terminal de comandos, vamos a la carpeta `themes` y desde ahí ejecutamos este comando:
```
git clone git@github.com:olOwOlo/hugo-theme-even.git
```
Esto nos descarga el tema Even en nuestro proyecto. Si ejecutaramos el comando para levantar nuestro sitio web
`hugo server -D`, y accedemos a la url que nos ha generado, no veríamos nada. Esto es debido a que no hemos configurado
nuestra web para que use el tema que acabamos de descargar.
Vamos al fichero de configuración (en la carpeta raíz del proyecto) `config.toml`, lo editamos y ponemos lo siguiente:



