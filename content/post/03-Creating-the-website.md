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
hugo new site demo-web
```
<!--more-->
Donde `demo-web` se corresponde con el nombre que yo he querido darle a mi nuevo sitio web. Puedes ponerle el nombre que quieras.

Una vez hecho esto, accedemos a la carpeta desde la terminal:
```
cd demo-web
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
`hugo server -D`, y accedemos a la url que nos ha generado (suele ser: `http://localhost:1313/`), no veríamos nada.
Esto es debido a que no hemos configurado
nuestro sitio para que use el tema que acabamos de descargar.

Esta configuración se hace en el fichero `config.toml`. Para ir rápido, vamos a copiar el contenido de `demo-web/themes/hugo-theme-even/exampleSite/config.toml`
y lo vamos a pegar en nuestro fichero config ubicado en la raíz del proyecto.

Ahora si, podríamos probar a levantar nuestro servidor web con Hugo:
```
hugo server -D

// Nos genera lo siguiente
                   | ES
+------------------+----+
  Pages            | 44
  Paginator pages  |  2
  Non-page files   |  0
  Static files     | 36
  Processed images |  0
  Aliases          | 15
  Sitemaps         |  1
  Cleaned          |  0

Total in 82 ms
Watching for changes in /demo-web/{content,data,i18n,layouts,static,themes}
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```

Y ya tendríamos nuestro sitio web disponible en http://localhost:1313/. Esta es la vista previa actual de nuestra web:

![Vista previa web](/img/03/preview.png)

En el siguiente post del blog, vamos a ver como dotar de contenido a nuestro sitio web. 👋





