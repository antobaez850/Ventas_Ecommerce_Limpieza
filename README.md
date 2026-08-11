# 🔄 Limpieza data set Ventas Ecommerce

### 📌 Objetivo

El dataset original (ventas_ecommerce.csv) contiene registros de pedidos de una empresa de e-commerce, con problemas típicos de calidad de datos que impiden un análisis confiable si no se corrigen previamente. El objetivo de esta etapa es dejar el dataset en condiciones de ser explorado y analizado sin que errores de carga, inconsistencias de formato o valores atípicos distorsionen los resultados, especialmente porque el análisis busca responder una pregunta de negocio concreta, y cualquier ruido en los datos puede llevar a conclusiones erróneas.

<hr/>

### ✅ La limpieza busca

• <b>Garantizar consistencia de formato:</b> unificando cómo se representan fechas y texto categórico (mayúsculas/minúsculas, espacios), para que valores que en realidad son iguales (ej. "web", " Web ", "WEB") no se traten como categorías distintas.

• <b>Eliminar redundancia:</b> removiendo duplicados exactos que inflarían artificialmente ciertos conteos o promedios.

• <b>Corregir errores de carga y de sistema:</b> como precios negativos (error de signo), valores que representan fallas técnicas (ej. dias_entrega = 999), o columnas calculadas que quedaron inconsistentes con sus variables de origen (ej. monto_total en 0 pese a tener precio y cantidad válidos).

• <b>Tratar valores atípicos (outliers):</b> sin descartar información válida, diferenciando entre valores extremos legítimos (ej. productos caros dentro de una categoría de precio alto) y errores de carga.

• <b>Gestionar valores faltantes:</b> evaluando en cada columna si conviene imputar (por mediana, moda o agrupado), asignar una categoría explícita como "Desconocido", o conservar el faltante como información en sí misma (como en el caso de rating, donde ausencia de calificación puede estar correlacionada con la variable de interés y no debe imputarse con un valor arbitrario).

<hr/>

### ⚙️ Implementación

<table>
  <tr>
    <th>Nombre</th>
    <th>Detalle</th>
  </tr>
  <tr>
    <td>Data set original</td>
    <td>ventas_ecommerce.csv</td>
  </tr>
  <tr>
    <td>Proceso limpieza Python</td>
    <td>Ventas_ecommerce_limpieza.ipynb</td>
  </tr>
  <tr>
    <td>Data set limpio</td>
    <td>ventas_ecommerce_clean.csv</td>
  </tr>
</table>


<hr/>

### 🔜 Próximos pasos

Realizar un análisis exploratorio utilizando el data set limpio para responder la siguiente pregunta de negocio:

<i>¿Qué categorías, canales o segmentos de clientes tienen mayor tasa de devolución y cómo se relaciona eso con el descuento aplicado y el tiempo de entrega? ¿Dónde conviene enfocar acciones para reducir devoluciones sin resignar ventas?</i>

