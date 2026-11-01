# Historias de usuario

Cada historia es un *issue* del repositorio vinculado al tablero de GitHub Projects. Salen del objetivo de la Entrega N.º 2 y de las metas M1 a M6.

## HU1 · Cargar el costo de cada producto

**Como** socio de la Dirección, **quiero** cargar y actualizar el costo de cada producto, **para** que la ganancia se calcule con valores reales aunque los precios de la mercadería cambien por la inflación.

**Criterios de aceptación**
- Todos los productos de los dos foodtrucks pueden tener un costo cargado (meta M2: 100 %).
- Actualizar el costo de un producto lleva 30 segundos o menos (M2).
- Cada venta guarda el costo vigente en ese momento, así un cambio de costo no altera las ventas pasadas.

## HU2 · Ver la ganancia por producto y por período

**Como** socio de la Dirección, **quiero** ver un reporte de ganancia por producto y por período (semana, mes y año), descontando las mermas, **para** saber qué productos dejan más ganancia y decidir precios y compras.

**Criterios de aceptación**
- Ganancia = ventas − costo de lo vendido − costo de las mermas.
- La ganancia del sistema coincide con un cálculo a mano con los mismos datos: $0 de diferencia (M3).
- El reporte mensual carga en 3 segundos o menos con 10.000 ventas (M4).

## HU3 · Acceso restringido a costos y ganancias

**Como** socio de la Dirección, **quiero** que solo la Dirección y el desarrollador puedan ver costos y ganancias, entrando con clave, **para** que esa información no la vea el personal ni aparezca en las capturas que se mandan al grupo de WhatsApp en cada cierre.

**Criterios de aceptación**
- Sin clave, el sistema oculta costos y ganancias (campo `ve_costos` de la entidad Usuario).
- Ninguna pantalla del personal ni captura del cierre muestra costos: 0 casos (M5).
- La carga de una venta sigue tardando 15 segundos o menos (M1).
