# Markdown 

Debido a que registraré la mayoría (por no decir todos) mis apuntes en Markdown, utilizaré la guía que ofrece GitHub para sus apuntes y así nutrirme de dicha información. La misma que me servirá a futuro para describir mis repositorios.

Las anotaciones se realizaran de acuerdo a las secciones que tiene el apartado ***Writing on GitHub[^1]*** de la introducción al uso de GitHub. El tutorial utiliza el editor de GitHub, sin embargo, lo realizaré con un editor de código

## Inicio rápido para escribir con GitHub[^2]

### Introducción
- Markdown es fácil de leer y escribir.
- Se puede usar junto a las etiquetas de HTML.

### Creación del README de perfil

1. Crear repositorio con el mismo nombre que el nombre usuario e inicializarlo con un archivo README
2. Edita el README 
> [!NOTE]
> Si creaste el archivo desde GitHub, debes eliminar la plantilla. Si ya existe un README es posible editarlo desde la página de perfil

### Imagen que se incorpora a los visitantes

Utilizando la etiqueta `picture`, se puede cambiar el color de las imágenes dependiendo del tema que esté utilizando el visitante.
```html
<picture>
 <source media="(prefers-color-scheme: dark)" srcset="IMAGEN_PARA_EL_MODO_OSCURO">
 <source media="(prefers-color-scheme: light)" srcset="IMAGEN_PARA_EL_MODO_CLARO">
 <img alt="TEXTO_ALTERNATIVO" src="IMAGEN_POR_DEFECTO">
</picture>
```
Las imágenes se deben colocar con URLs. Para mayor accesibilidad se recomienda colocar un texto alternativo a la imagen.

### Incorporar una tabla

Las tablas son útiles para organizar información. Un ejemplo de tabla es el siguiente.

```markdown
| Rank | COSA_PARA_RANKEAR |
|-----:|-------------------|
|     1|                   |
|     2|                   |
|     3|                   |

```
La secuencia `--:` indica que la alineación sea a la derecha. Con `:--` la alineación sería a la izquierda. Por defecto, la alineación es central.

### Incorporar una sección contraída

Se utiliza la etiqueta `details` de HTML.
```markdown
<details>
<summary>TEXTO_CORTO_INICIAL</summary>
TU_INFORMACIÓN_DETALLADA
</details>
```

Si se desea que la sección se muestre abierta de forma predeterminada se utiliza `<details open>`
Ejemplo:
<details>
<summary>Mis lenguajes</summary>

| Rank | Lenguajes |
|-----:|-----------|
|     1| JavaScript|
|     2| Python    |
|     3| SQL       |

</details>

### Incorporar una cita

Para aplicar formato en este caso específico a una cita, se agregará una regla horizontal y un bloque de comentario

```markdown
---
> CONTENIDO
— AUTOR
```

> Para escribir el guión largo CTRL + SHIFT + U, luego escribir "2014" y Enter.

### Incorporar un comentario

Utilizar la sintaxis de HTML para el comentario

```html
<!-- COMENTARIO -->
```

## Acerca de escritura y formato GitHub[^3]

GitHub agrega funcionalidades personalizadas para crear el formato de Markdown de GitHub. Se puede hacer menciones, referencias de incidencia, solicitudes de cambios, emojis, entre otros.

### Barra de herramientas de formato de texto

Cada campo de comentario en GitHub tiene herramientas de formato de texto, lo que puede ser útil en varios casos e incluso permite aplicar formato sin necesidad de aprender Markdown.

### Habilitar fuentes de ancho fijo

Cada carácter tendrá el mismo espacio horizontal, lo que facilitará la edición de estructuras avanzadas.
1. En la foto de perfil, hacer click y luego a *Configuraciones*
2. En la barra lateral izquierda, click en *Apariencia*
3. En *Preferencia de fuente del editor de Markdown*, seleccionar *Usar fuente de ancho fijo*

## Sintaxis de escritura y formato básicos[^4]

### Encabezados

Agregar entre uno a seis símbolos `#` antes del texto. Esto determina el nivel jerárquico tal como HTML.

```markdown
# Primer nivel
## Segundo nivel
### Tercer nivel
```

GitHub genera automáticamente una tabla de contenido a la que se puede acceder desde el menú.

### Estilos de texto

|Estilo    |Sintaxis    |Abrev. Linux|Ejemplo     |Resultado   |
|:---------|:-----------|:-----------|:-----------|:-----------|
|Negrita|`** **` o `__ __`|`Ctrl`+`B`|`**Bold Text**`|**Bold Text**|
|Cursiva|`* *` o `_ _`|`Ctrl`+`I`|`_Italic Text_`|_Italic Text_|
|Tachado|`~~ ~~`|Ninguno|`~~Bad Text~~`|~~Bad Text~~|
|Cursiva en negrita y anidada|`** **` y `_ _`|Ninguno|`**Texto _muy_ importante**`|**Texto _muy_ importante**|
|Todo en negrita y cursiva|`*** ***`|Ninguno|`***Todo es importante***`|***Todo es importante***|
|Subíndice|`<sub> </sub>`|Ninguno|`Texto <sub>subíndice</sub>`|Texto <sub>subíndice</sub>|
|Superíndice|`<sup> </sup>`|Ninguno|`Texto <sup>superíndice</sup>`|Texto <sup>superíndice</sup>|

> [!NOTE]
> En mi caso, no me dejaba colocar correctamente el tachado en el README con `~~ ~~`, pero siempre es posible hacerlo con `<s>`, `<del>` o `<strike>`. Los comandos funcionan cuando te encuentras en el editor de GitHub

### Citas

Puedes citar con `>`. A las citas se le aplican sangría y tienen un color diferente.
Ejemplo:
```markdown
Esto no es una cita
> Esto es una cita
```

Esto no es una cita
> Esto es una cita

### Bloques y líneas de código

Dentro de comillas inversas se puede insertar código. Un método abreviado en el editor de GitHub es `Ctrl`+`E`.
Ejemplo:
```markdown
Usar `git  status`
```

Usar `git status`

Para un bloque de código se utilizan tres comillas inversas.
Ejemplo:
````markdown
Comandos básicos de Git:
```
git status
git add
git commit
```
````

Comandos básicos de Git:
```markdown
git status
git add
git commit
```

> [!NOTE]
> Si te preguntas como se hace para representar el bloque de código de Markdown dentro de un bloque de código como fue el ejemplo anterior. La respuesta es que también se pueden utilizar cuatro comillas inversas para el bloque de código. Igualmente, en la parte final de esta sección hablaremos de como saltar código Markdown. Por otra parte, se puede hacer resaltado de sintaxis colocando el nombre del lenguaje luego de las comillas, de esta manera: ` ```html `. Sin embargo ese es tema de otra sección.

### Colores

Puede ocurrir que en las issues y pull requests se hagan referencia a colores. GitHub admite sintaxis que muestra una previsualización del color.
Ejemplo:
```markdown
El color de fondo es `#ffffff` para el modo claro y `#000` para el modo oscuro.
```

El color de fondo es `#ffffff` para el modo claro y `#000` para el modo oscuro.

Los modelos de color admitidos actualmente (Junio 2024) son:
|Color|Sintaxis|Ejemplo|Resultados|
|-|-|-|-|
|HEX|``` `#RRGGBB` ```|``` `#0969DA` ```|`#0969DA`|
|RGB|``` `rgb(R,G,B)` ```|``` `rgb(9, 105, 218)` ```|`rgb(9, 105, 218)`|
|HSL|``` `hsl(H,S,L)` ```|``` `hsl(212, 92%, 45%)` ```|`hsl(212, 92%, 45%)`|

> [!NOTE]
> El color no puede tener espacios iniciales o finales dentro de comillas simples. La visualización del color solo se admite en pull request e issues. Por lo que es casi seguro que en estos ejemplos no se muestre la visualización. Te recomiendo probarlo en una issue o pull request

### Vínculos

Se debe escribir el texto entre corchetes `[ ]` y la URL entre paréntesis `( )`. En el editor de GitHub, se puede utilizar el comando `Ctrl`+`k`.
Ejemplo:
```markdown
Hacia [GitHub Pages](https://pages.github.com/)
```

Hacia [GitHub Pages](https://pages.github.com/)

> [!NOTE]
> GitHub crea vínculos automáticamente cuando las direcciones URL se escriben como comentario

### Vínculos relativos

Es un enlace que inicia el camino de su referencia en la ubicación del archivo actual.Por ejemplo, si estamos en el README y queremos referenciar *docs/WIKI.md*
```markdown
[Wiki para este proyecto](docs/Wiki.md)
```
> [!IMPORTANT]
> El texto del vínculo debe estar en una sola línea. 

GitHub trasformará de manera automática el enlace relativo en cualquier rama en la que te encuentres, para que siempre funcione correctamente. Los enlaces relativos son más sencillos para los usuarios que clonan tu repositorio. Se recomienda usar enlaces relativos para consultar archivos dentro del repositorio

### Imágenes

Para agregar una imagen basta usar `!` antes de la sintaxis del vínculo. Dentro de los corchetes estará el texto alternativo.
Ejemplo:
```markdown
![Mi foto de perfil](https://avatars.githubusercontent.com/gusCreator)
```

![Mi foto de perfil](https://avatars.githubusercontent.com/gusCreator)

> [!NOTE]
> Cuando quieras mostrar una imagen incluida en un repositorio, usa vínculos relativos en vez de absolutos.

### Listas

Para listas sin ordenar se debe colocar `-`, `*` o `+` antes de una o más lineas de texto.

```markdown
- George Washington
* John Adams
+ Thomas Jefferson
```
- George Washington
* John Adams
+ Thomas Jefferson

Para ordenar la lista, antecede cada línea con un número

1. James Madison
2. James Monroe
3. John Quincy Adams


#### Listas anidadas

Las listas anidadas se crean puramente con sangría, tanto para fuentes de ancho fijo (monoespaciada) o que no son de ancho fijo. Se debe contar el número de caracteres desde que empieza el contenido del elemento de la lista padre, ese lugar es donde se coloca la lista anidada. Claramente, en fuentes de ancho fijo se tendrá una ayuda visual para este proceso.
Ejemplos:
```markdown
100. Lista padre
     - Lista anidada
```
100. Lista padre
     - Lista anidada
     
```markdown
100. Lista padre
       - Lista anidada
         - Lista hija
```
100. Lista padre
       - Lista anidada
         - Lista hija
         
         
### Lista de tareas

Para declarar esta lista se coloca
```markdown
- [x] Comer
- [ ] Dormir
- [ ] Jugar
```
- [x] Comer
- [ ] Dormir
- [ ] Jugar
Se marca con `x` para indicar que está realizado.

### Mencionar personas y equipos

Se escribe `@` y luego el nombre de usuario o del grupo para hacer una mención. Esto activa una notificación si es que el mencionado tiene acceso de lectura al repositorio o si pertenece a la organización.
En el editor de GitHub, cuando haces estas menciones, mientras de escribe se van filtrando las opciones.

### Emojis

Se utilizan los códigos de los emojis `:CÓDIGO_DE_EMOJI:`
```markdown
:+1: Luce genial 
```
:+1: Luce genial 

> Consulta la hoja de referencia rápida de los emojis[^5]

### Notas al pie

Se utiliza la sintaxis entre corchetes.
```markdown
Ir a referencia[^6]
[^6]: Esta es la referencia 6
```
Ir a referencia[^6]
[^6]: Esta es la referencia 6

> [!NOTE]
> La nota al pie **siempre** se representará en la parte final del archivo. Las notas al pie no se admiten en las wikis.

### Alertas

Se utilizan para representar información crítica. En GitHub se muestran con colores distintivos. Es importante tratar de reducir el uso de estas alertas para evitar sobrecargar al lector.
```markdown
> [!NOTE]
> Recomendaciones y cosas que el usuario debería saber

> [!TIP]
> Recomendación para hacer las cosas más fáciles

> [!IMPORTANT]
> Información que los usuarios necesitan conocer para lograr su objetivo

> [!WARNING]
> Información que necesita ser atendida inmediatamente por el usuario para evitar problemas

> [!CAUTION]
> Riesgos o resultados negativos de determinadas acciones
```
> [!NOTE]
> Recomendaciones y cosas que el usuario debería saber

> [!TIP]
> Recomendación para hacer las cosas más fáciles

> [!IMPORTANT]
> Información que los usuarios necesitan conocer para lograr su objetivo

> [!WARNING]
> Información que necesita ser atendida inmediatamente por el usuario para evitar problemas

> [!CAUTION]
> Riesgos o resultados negativos de determinadas acciones


### Ignorar formato Markdown

Se puede ignorar caracteres Markdown anteponiendo `\` antes del caracter.
```markdown
Usemos asteriscos  \*aquí\*
```
Usemos asteriscos  \*aquí\*

El formato no se puede omitir en el título de una issue o de una pull request

### Ver código Markdown en GitHub

Al ver la presentación se debe hacer click en la pestaña `Code` del archivo. Con esto se puede utilizar las características de vista del código fuente.

[^1]: Visitar [Artículo](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github)
[^2]: Visitar sección [Inicio rápido](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)
[^3]: Visitar sección [Acerca de escritura y formato](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/about-writing-and-formatting-on-github)
[^4]: Visitar sección [Sintaxis de escritura y formatos básicos](https://docs.github.com/es/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
[^5]: Visitar [Hoja de referencia rápida de los emoji](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)
