# Visor INN · Datos de entrada

App de un solo archivo HTML para ver el Excel `INN_Datos_Entrada.xlsx` del subgrupo de Innovación. No usa librerías, no necesita instalación ni internet: el Excel se lee directamente en el navegador y no sale del equipo.

## Uso

1. Abre `INN_Visor_Datos.html` en Edge o Chrome (doble clic o desde GitHub Pages).
2. Pulsa **Elegir Excel** y selecciona `INN_Datos_Entrada.xlsx`, o arrástralo a la ventana.
3. Cuando cambies el Excel, **guárdalo** y pulsa **Actualizar**: la app vuelve a leer el mismo archivo.
4. La casilla **auto (5 s)** recarga sola cada vez que se guarda el Excel.

Al reabrir la app recuerda el último archivo; el primer clic en Actualizar pide permiso de lectura. En Firefox y Safari, Actualizar vuelve a abrir el selector de archivo.

## Qué muestra

- **Resumen**: ideas por tipo, horas liberadas y ahorro en CLP (por separado), cartera por estado y plataforma, observaciones por tipo, historias por versión, comité por caso de negocio y tipo declarado, y beneficio estimado vs. real (horas, CLP y adopción).
- **Una pestaña por hoja de datos**, con búsqueda y orden por columna.
- **Referencia**: hojas Instrucciones, Metadata_paquete, Flujo y Diccionario.

## Formato esperado del Excel

En cada hoja de datos: fila 1 título con `Origen:`, fila 2 descripción, fila 3 origen por columna, fila 4 encabezados y datos desde la fila 5. Se leen todas las filas con datos, aunque queden fuera del rango de la tabla de Excel, y las columnas nuevas aparecen solas. Las columnas que empiezan con `Fecha` se muestran como DD-MM-AAAA y las que contienen `CLP` como montos en pesos.

## Requisitos

Navegador actual con `DecompressionStream` (Chrome/Edge 103+, Firefox 113+, Safari 16.4+). La relectura del mismo archivo usa la File System Access API (Chrome y Edge).
