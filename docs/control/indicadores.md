# Indicadores de control y estándares de desempeño

Las metas de la Entrega N.º 2 dicen qué tiene que lograr el proyecto. Estos indicadores sirven para controlar, una vez en producción, que el sistema siga cumpliendo. Cada uno sigue el ciclo de control: **estándar → medición → comparación → acción correctiva**.

| N.º | Indicador | Cómo se mide | Estándar | Frecuencia | Responsable | Si no se cumple |
|---|---|---|---|---|---|---|
| IC1 | Tiempo de carga de una venta | Cronometrar un pedido típico (hasta 3 productos) en hora pico | 15 s o menos | Una vez por semana | Desarrollador | Revisar y simplificar la pantalla de venta |
| IC2 | Costos al día | Productos con costo actualizado en los últimos 30 días / total de productos | 100 % | Una vez por mes y con cada aumento de un proveedor | Dirección | El reporte marca los productos con costo viejo y el socio responsable de esa mercadería lo actualiza |
| IC3 | Exactitud de la ganancia | Diferencia entre la ganancia del sistema y un cálculo a mano de 10 productos | $0 | Una vez por mes | Desarrollador y Dirección | Revisar la fórmula y los costos guardados en las ventas |
| IC4 | Velocidad del reporte | Tiempo de carga del reporte mensual con 10.000 ventas | 3 s o menos | En cada versión nueva | Desarrollador | Optimizar el cálculo antes de publicar la versión |
| IC5 | Privacidad de los costos | Pantallas del personal y capturas del cierre que muestran costos o ganancias | 0 | En cada cierre y en cada versión nueva | Desarrollador | Corregir el permiso y cambiar la clave |
| IC6 | Diferencia de caja | Efectivo esperado según el sistema vs. efectivo contado en el cierre | $0, o diferencia explicada en el cierre | En cada cierre | Caja y Dirección | Revisar las ventas editadas y los retiros del día |

## Cómo se relacionan con las metas

| Indicador | Meta de la Entrega N.º 2 |
|---|---|
| IC1 | M1 · Rapidez de venta |
| IC2 | M2 · Carga de costos |
| IC3 | M3 · Exactitud de la ganancia |
| IC4 | M4 · Velocidad del reporte |
| IC5 | M5 · Privacidad de los costos |
| IC6 | Control del cierre de caja (proceso del BPMN) |
