---
title: "About"
date: 2018-02-27T18:01:35+01:00
draft: false
comment: true
menu: "main"
weight: 50
---

### ¡Hola!

Esta es la página de about. Ha sido creada a través de Hugo, con el comando `> hugo create about.md`  
La página de _about_ tenía este contenido inicialmente:
```
---
title: "About"
date: 2018-02-27T18:01:35+01:00
draft: true
---
```

Estos son los metadatos que se generan automáticamente cuando usamos el comando de `hugo`.
Estos metadatos puede editarse para personalizar aun más nuestra página.
```
---
title: "About"                         # Título
date: 2018-02-27T18:01:35+01:00        # Fecha de creación
draft: true                            # Borrador ?
comment: true                          # Comentarios ?
menu: "main"                           # Menu principal ?
weight: 50
---
```

Estos datos cambian segun el _theme_ que tengamos instalado.
Seguramente, no todos los temas tengan soporte para comentarios con **Disqus**. En el fichero de configuración (`config.toml`)
hemos rellenado las variables que nos interesaban. En este caso, para usar disqus, usado la variable **DisqusShortname**.

Vamos a ver como se usaría esto con el sistema de templates de Hugo. En el siguiente código tenemos unos _if_ (condicionales)
junto con unas variables:

```markdown
# Condición 1:
# Si es de "tipo Page" y el meta dato de "comment" es distinto (ne: not equal) de false, entonces seguimos
# Condición 2:
# Si la variable "DisqusShortname" existe y tiene valor (distinto de vacío)

{{ if and .IsPage (ne .Params.comment false) }}                     # Condición 1
  <!-- Disqus -->
  {{- if .Site.DisqusShortname -}}                                  # Condición 2
  ...
  {{- end }}
  ...
{{- end }}
```
