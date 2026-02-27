primerpromt:

Quiero crear la estructura HTML de un ejercicio de layout.
Necesito que generes un documento HTML5 semánticamente correcto. Debe incluir:
- Declaración <!DOCTYPE html>
- Elemento <html> con atributo lang
- Secciones <head> y <body>
- Meta charset UTF-8
- Un título en el documento
Dentro del body debe existir un contenedor principal que represente un componente visual.
Requisitos de estructura:
- El contenedor principal debe representarse con un elemento semántico apropiado (por ejemplo <main> o <section>).
- Dentro del contenedor deben existir 8 elementos que representen figuras geométricas:
  - 4 cuadrados
  - 4 círculos
Para mantener una buena organización y especificidad de estilos, cada figura debe tener clases CSS separadas.
Ejemplo de organización de clases:
square
circle
y clases adicionales para posicionamiento como:
s1, s2, s3, s4
c1, c2, c3, c4
No agregues estilos complejos todavía. Solo la estructura HTML y el enlace a un archivo CSS externo llamado style.css.


segundo promt:

Ahora quiero que generes el archivo style.css para el HTML anterior.
Objetivos de esta etapa:
Aplicar estilos base usando conceptos de CSS como:
- Modelo de caja (box model)
- Especificidad de selectores
- Unidades relativas y absolutas
- Reseteo básico de márgenes
Requisitos del CSS:
1. Reset básico
El body debe eliminar márgenes por defecto y usar:
margin: 0;
2. Fondo de la página
El fondo de la página debe ser oscuro para generar contraste visual con el contenedor central.
3. Contenedor principal
El contenedor principal debe tener:
- width: 400px
- height: 300px
- background color azul
- box-sizing: border-box
- position: relative (para permitir posicionamiento absoluto de hijos)
4. Figuras geométricas
Crear dos clases base:
.square
.circle
Ambas deben:
- usar el modelo de caja estándar
- tener dimensiones iguales usando unidades px o rem
- aproximadamente 50px o 3rem
Los cuadrados deben tener color celeste.
Los círculos deben tener color rosado y usar:
border-radius: 50%
5. Organización de clases
Las clases base (.square y .circle) deben definir los estilos compartidos.
Las clases adicionales (s1, s2, c1, etc.) se usarán posteriormente para el layout.
No agregues aún posicionamiento ni layout avanzado.

tercer promt:

Ahora quiero refinar el layout para que coincida exactamente con el diseño visual.
Debes utilizar conceptos avanzados de CSS como:
- Flexbox
- flex-direction
- alineación con justify-content y align-items
- position absolute dentro de un contenedor relativo
Objetivos del layout:
1. Centrar el contenedor en el viewport
El body debe usar Flexbox para centrar el contenedor.
Requisitos:
display: flex
justify-content: center
align-items: center
height: 100vh
Esto permite que el contenedor permanezca centrado independientemente del tamaño del viewport.
2. Posicionamiento interno
El contenedor debe actuar como contexto de posicionamiento usando:
position: relative
Todas las figuras deben usar:
position: absolute
para posicionarse respecto al contenedor.
3. Distribución de figuras
Las figuras deben ubicarse en las cuatro esquinas internas del contenedor.
Distribución:
Arriba izquierda:
cuadrado seguido de círculo
Arriba derecha:
círculo seguido de cuadrado
Abajo izquierda:
círculo seguido de cuadrado
Abajo derecha:
cuadrado seguido de círculo
4. Separación interna
Debe existir un espacio interno desde los bordes del contenedor (aproximadamente 20px).
Para lograrlo se deben usar propiedades como:
top
bottom
left
right
5. Clases específicas
Cada figura debe usar su clase específica para definir su posición:
.s1
.s2
.s3
.s4
.c1
.c2
.c3
.c4
Esto ayuda a controlar la especificidad y mantener el CSS organizado.
6. Restricción importante
Ninguna figura puede salir del contenedor.
usar:
overflow: hidden
en el contenedor para garantizar esto.