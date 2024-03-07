# Desafio_AlgoritmoML_MVP_Forte
En esta entrega entrenamos un modelo de regresión logística para predecir la variable "order" en nuestro dataset de una farmacia online.

#**Introduccion**

El dataset con el que vamos a trabajar recopila datos de ventas y actividad de los clientes en el sitio web de una farmacia online a lo largo de 90 días.

Tenemos información sobre varias características de los productos que serán detalladas en secciones siguientes, sus precios, los precios de la competencia y comportamiento de los clientes, si hacen click en un producto, si los colocan en una canasta de productos y finalmente si compran un producto. Nótese que no todas las líneas representan ventas.

La clave del dataset es que la farmacia sigue una política de 'pricing dinámico' donde los precios de cada producto son ajustados diariamente, dentro de ciertas bandas

#**Objetivos y estrategia de estimación**

En este trabajo vamos a enfocarnos en predecir si, dadas las características cada observación o fila del dataset, se va a producir una venta o no.

Recordemos que tenemos una variable llamada Order que toma valores 0 y 1, cuando order==1, la observación representa una venta, y cuando toma el valor 0 no se trata de una venta.

Siendo que nuestra variable dependiente es categórica y toma valores 0 (no-venta) y 1 (venta) vamos a proponer un modelo de regresión logística.

En otros trabajos el foco ha estado en predecir el revenue, y se ha demostrado en la segunda pre-entrega que el modelo de regresión lineal simple no es apropiado para nuestra estructura de datos, sólo como muestra, el r2 era de
~0.5.

Estimar la probabilidad de ventas, aparte de ser una pregunta de investigación importantísima en sí misma, puede funcionar como paso intermedio para estimar el revenue. Para ver por qué, recordemos que el revenue surge de las cantidades vendidas multiplicadas por el precio. El dataset contiene los precios, y la cantidad vendida en el set de testing se puede obtener construyendo una variable dividiendo revenue por precio, de modo que, si logramos predecir correctamente las ventas, podremos calcular el revenue.

