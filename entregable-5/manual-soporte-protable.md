# Manual de soporte de ProTable para locales gastronómicos

| Dato | Valor |
|---|---|
| Documento | Manual de soporte de ProTable para locales gastronómicos |
| Versión | 1.0 |
| Fecha de vigencia | 11 de octubre de 2026 |
| Responsable del contenido | Bruno Acorsi (ProTable) |
| Uso | Base de conocimiento oficial del asistente de soporte de ProTable |
| Fuentes | FAQ público de protable.io, condiciones comerciales vigentes y documentación funcional del producto |

## 1. Qué es ProTable

### 1.1 ProTable en una oración

ProTable es un sistema de pedidos y pagos por código QR para gastronomía: restaurantes, bares y cafeterías, locales de take away y delivery, y espacios de eventos o recreación como cable parks, playas y festivales.

### 1.2 Cómo funciona ProTable

En ProTable, el local carga su menú y personaliza su logo y sus colores. Cada mesa tiene un código QR único: el cliente lo escanea con la cámara de su celular y entra a la carta desde el navegador, sin instalar ninguna aplicación ni registrarse. El cliente pide, puede dividir la cuenta y paga desde su celular con MercadoPago o en efectivo. El pedido llega directo a la cocina o a la barra, sin pasar por el mozo.

### 1.3 Marca blanca

ProTable funciona como marca blanca: el cliente del local nunca ve la marca ProTable, sino la del negocio. El local personaliza el logo, los colores, las fotos de los platos, las descripciones y los alérgenos.

### 1.4 Qué no reemplaza ProTable

ProTable no reemplaza el sistema de punto de venta (POS) ni el sistema de facturación del local: los complementa. Los pedidos entran por ProTable y la cocina los recibe en el tablero Kanban; el local puede seguir usando su propio sistema de facturación. ProTable tampoco reemplaza a los mozos: los libera de tomar pedidos para que se concentren en la atención.

### 1.5 Métricas del negocio

ProTable ofrece un panel con métricas en tiempo real: ventas del día, ticket promedio, productos más vendidos y horarios pico. Los reportes se pueden exportar.

## 2. Planes y precios

### 2.1 Tabla de planes de ProTable

| Plan | Precio mensual | Qué incluye |
|---|---|---|
| Starter | $25.000 por mes | Menú QR y pedidos, hasta 15 mesas, pantalla de cocina y barra (KDS), pedidos para llevar, métricas, pagos con MercadoPago y soporte por email |
| Pro (el más elegido) | $50.000 por mes | Mesas ilimitadas, modo take away (walk-in), notificaciones por WhatsApp, tablero Kanban, división de la cuenta y soporte prioritario |
| Enterprise | A medida | Varias sucursales, acceso a API, marca blanca completa, nivel de servicio garantizado y un responsable de cuenta dedicado |

### 2.2 Condiciones comunes a todos los planes

Todos los planes de ProTable incluyen 15 días de prueba gratis, sin tarjeta de crédito. ProTable no cobra comisión sobre las ventas del local. No hay contratos largos: el plan se puede cancelar en cualquier momento.

### 2.3 Cuánto cuesta ProTable

ProTable cuesta desde $25.000 por mes (plan Starter). El plan Pro cuesta $50.000 por mes y el plan Enterprise se cotiza a medida. Todos tienen 15 días de prueba gratis y ninguno cobra comisión sobre las ventas.

## 3. Preguntas frecuentes

### 3.1 Qué necesita un local para empezar

Para empezar a usar ProTable, el local solo necesita conexión a internet y un dispositivo para ver los pedidos: una tablet, una notebook o un celular. Los clientes usan su propio celular para escanear el QR. No hace falta comprar hardware.

### 3.2 El cliente no necesita descargar una aplicación

En ProTable, el cliente no descarga ninguna aplicación ni se registra. Escanea el código QR y entra directo a la carta desde el navegador del celular.

### 3.3 Cómo funcionan los pagos

En ProTable, el local conecta su cuenta de MercadoPago en tres clics. Los pagos van directo a la cuenta de MercadoPago del local: ProTable nunca toca el dinero. El local también puede trabajar solo con efectivo.

### 3.4 Es seguro pagar desde el celular

Sí. En ProTable, los pagos se procesan íntegramente a través de MercadoPago, que cuenta con certificación PCI DSS. ProTable nunca ve ni guarda datos de tarjetas.

### 3.5 Cómo recibe el local el dinero de las ventas

El dinero de las ventas pagadas con MercadoPago llega directo a la cuenta de MercadoPago del local, como cualquier otra venta. ProTable no intermedia ni retiene fondos.

### 3.6 Propinas

En ProTable, el cliente puede dejar una propina digital al pagar. La propina se registra por separado para que el personal la reciba.

### 3.7 Personalizar el menú y los colores

Sí, se puede. En ProTable, el local personaliza el logo, los colores, las fotos de los platos, las descripciones y los alérgenos. Es 100 % marca blanca: el cliente ve la marca del local, no la de ProTable.

### 3.8 ProTable no reemplaza a los mozos

ProTable no reemplaza a los mozos. Los libera de tomar pedidos para que se enfoquen en la atención, reduce los errores y mejora la eficiencia del salón.

### 3.9 Usar ProTable junto con el POS actual

Sí. ProTable no reemplaza el POS del local, lo complementa: los pedidos entran por ProTable, la cocina los recibe en el tablero Kanban y el local puede seguir usando su sistema de facturación.

### 3.10 Qué datos del negocio puede ver el local

En ProTable, el local ve un panel en tiempo real con las ventas del día, el ticket promedio, los productos más vendidos y los horarios pico. Los reportes se pueden exportar.

### 3.11 Qué soporte ofrece ProTable

ProTable ofrece soporte por email y por WhatsApp, y un Centro de Ayuda con guías paso a paso dentro del panel. El plan Pro incluye soporte prioritario.
## 4. Pedido desde la mesa con código QR

### 4.1 Qué necesita una mesa para recibir pedidos

En ProTable, el cliente solo puede pedir desde una mesa que el personal del local abrió antes desde el panel. Si la mesa no está abierta (ocupada), el cliente que escanea el QR ve la pantalla "Mesa no disponible" y no puede ver el menú para pedir. Por eso, cuando se sientan los comensales, el primer paso es abrir la mesa desde la sección Mesas del panel (ver la sección 12).

### 4.2 Cómo entra el cliente: el código QR de la mesa

En ProTable, cada mesa tiene su propio código QR, que se genera e imprime desde el panel. El QR identifica a esa mesa en particular (no solo su número) y lleva al cliente directo al menú de esa mesa. El cliente lo escanea con la cámara de su celular; no necesita instalar ninguna aplicación. ProTable también tiene una pantalla de escaneo manual: no abre la cámara, sino que muestra instrucciones para usar la cámara del celular y permite ingresar el identificador de la mesa a mano. Si ese identificador no corresponde a ninguna mesa, aparece el mensaje "Mesa no encontrada".

### 4.3 Navegar el menú y armar el carrito

En ProTable, el menú que ve el cliente muestra solo las categorías activas y los productos marcados como disponibles, en el orden que definió el local. Las categorías pueden tener subcategorías: al elegir una categoría, el cliente ve los productos de esa categoría y de todas las que dependen de ella. Arriba del menú puede aparecer un carrusel de promociones con hasta 5 productos destacados. El menú toma los colores del local y, si el local cargó una imagen de fondo, la muestra en forma tenue. El cliente agrega productos al carrito y lo abre con el botón flotante del carrito.

### 4.4 Cubierto y cantidad de comensales

En ProTable, si el local cobra cubierto, al confirmar el primer pedido de la mesa el sistema le pregunta al cliente cuántos comensales son. El total del cubierto se calcula como la cantidad de comensales multiplicada por el valor del cubierto del local. Esta pregunta aparece una sola vez por mesa: los pedidos siguientes de la misma mesa ya no la muestran. Si el local no cobra cubierto, la pregunta no aparece.

### 4.5 Confirmar el pedido desde la mesa

En ProTable, cuando el cliente confirma el carrito en una mesa, el pedido se envía al local con estado Pendiente y aparece en el tablero Kanban del panel. El cliente no paga en ese momento: en la mesa se pide primero y se paga al final, cuando el cliente decide pagar la cuenta. Después de enviar el pedido, el carrito se vacía y el cliente pasa a la pantalla de sus pedidos, donde ve el estado de lo que pidió. Si el sistema no logra identificar el local de la mesa, muestra el mensaje "No se pudo identificar el restaurante de esta mesa. Volvé a escanear el QR."

### 4.6 Pedir de nuevo en la misma mesa

En ProTable, el cliente de una mesa puede hacer varios pedidos durante la misma visita. Desde la pantalla de sus pedidos, el botón "Agregar" lo lleva de vuelta al menú de la mesa. Todos los pedidos de la mesa se suman a la misma cuenta. El botón "Agregar" deja de mostrarse cuando la cuenta de la mesa ya está pagada.

### 4.7 El carrito no se guarda si se recarga la página

En ProTable, el carrito del cliente se guarda solo mientras la página está abierta. Si el cliente recarga la página antes de confirmar, pierde los productos que tenía en el carrito y tiene que volver a agregarlos. La mesa, en cambio, no se pierde: el celular la recuerda y el cliente sigue en la misma mesa.

## 5. Pedido take away / walk-in

### 5.1 Qué es un pedido take away en ProTable

En ProTable, un pedido take away (también llamado walk-in) es un pedido sin mesa. El cliente entra por un link público del local, deja su nombre y su teléfono, arma su pedido, paga antes de que se prepare y sigue su pedido por número. Este tipo de pedido tiene que estar habilitado para el local; si no lo está, el link no lleva al menú.

### 5.2 Link del local e identificación del cliente

En ProTable, cada local que tiene habilitado el take away tiene un link público propio. Al entrar, el cliente completa un formulario con nombre y teléfono, y los dos datos son obligatorios. Recién después de identificarse ve el menú, que funciona igual que el de la mesa (mismas categorías, productos y carrito). Si el link no corresponde a ningún local o el local no tiene el take away habilitado, el menú no se muestra. Si hay un problema de conexión, la pantalla ofrece un botón "Reintentar".

### 5.3 Número de pedido take away

En ProTable, cada pedido take away recibe un número de pedido del local cuando el cliente confirma el carrito. Ese número sirve para identificar el pedido en el mostrador y para que el cliente lo busque después en la pantalla de seguimiento. El cliente también puede buscar su pedido con el teléfono que dejó al identificarse.

### 5.4 Tipo de entrega en un pedido take away

En ProTable, el cliente de take away elige el tipo de entrega en la pantalla de pago, antes de pagar. Elegir el tipo de entrega es obligatorio: si el cliente intenta pagar sin elegirlo, el sistema le marca el error y lo lleva a esa parte de la pantalla. Las opciones dependen de cómo configuró el local el take away, por ejemplo los puntos de retiro disponibles y, si el local lo permite, la posibilidad de indicar una ubicación.

### 5.5 El pedido take away se paga antes de prepararse

En ProTable, un pedido take away no pasa a cocina hasta que está pagado. Mientras no se confirma el pago, el pedido aparece en la columna "En Caja" del tablero Kanban y el personal no puede avanzarlo. Si el cliente pagó con MercadoPago, el pedido pasa a Pendiente cuando se confirma el pago. Si el cliente eligió efectivo, ve el mensaje "Tu pedido es el #N. Acercate a la caja para pagar." y el pedido queda en "En Caja" hasta que el personal confirma el cobro desde el tablero. En take away no se puede dividir la cuenta: se paga el total.

### 5.6 Diferencias entre pedido en mesa y pedido take away

| | Pedido en mesa | Pedido take away / walk-in |
|---|---|---|
| Cómo entra el cliente | Escanea el código QR de su mesa | Entra por el link público del local |
| Requisito previo | El personal tiene que haber abierto la mesa desde el panel | El local tiene que tener el take away habilitado |
| Cómo se identifica el cliente | Por la mesa; no deja nombre ni teléfono | Con nombre y teléfono obligatorios, y recibe un número de pedido |
| Cubierto | Si el local cobra cubierto, se pregunta la cantidad de comensales en el primer pedido | No aplica |
| Cuándo se paga | Al final, cuando el cliente decide pagar la cuenta; puede hacer varios pedidos antes | Antes de que el pedido pase a cocina |
| Dividir la cuenta | Sí: partes iguales, por ítems o monto personalizado | No: se paga el total |
| Dónde aparece primero en el Kanban | En Pendientes | En "En Caja", hasta que se confirma el pago |
| Cómo sigue su pedido | En la pantalla de pedidos de la mesa, agrupado por estado | En una pantalla de seguimiento propia, con el número de pedido; se puede buscar por número o por teléfono |

## 6. Estados de un pedido

### 6.1 Tabla de estados de un pedido

En ProTable, cada pedido pasa por estos estados. Los nombres de la columna "Estado" son los que usa el tablero Kanban del panel.

| Estado | Qué significa | Quién lo cambia / cuándo |
|---|---|---|
| En Caja | Pedido take away que todavía no está pagado. No es un estado propio del pedido: es una columna del tablero Kanban que agrupa los pedidos take away en Pendiente con saldo sin pagar | Sale de "En Caja" cuando se confirma el pago: automáticamente si el cliente pagó con MercadoPago, o cuando el personal confirma el efectivo desde el tablero |
| Pendiente | El pedido llegó al local y espera que lo empiecen a preparar | Se crea así cuando el cliente confirma el pedido en la mesa, o cuando se confirma el pago de un take away. El personal lo avanza con el botón "Preparar" |
| En preparación | El pedido se está preparando | El personal lo pasa a "Listo" con el botón "Listo" |
| Listo | El pedido está listo para entregar | El personal lo pasa a "Entregado" con el botón "Entregado" |
| Entregado | El pedido se entregó al cliente | Estado final. Los entregados se ven en el tablero durante 24 horas y después desaparecen solos |
| Cancelado | El pedido se canceló | El personal lo cancela desde la tarjeta del tablero, con confirmación. Se puede cancelar en cualquier estado salvo Entregado o Cancelado. Los cancelados no se muestran en el tablero Kanban |

### 6.2 La columna "En Caja" del tablero Kanban

En ProTable, "En Caja" es una columna del tablero Kanban, no un estado guardado del pedido. Muestra los pedidos take away que están en Pendiente y todavía tienen saldo sin pagar. Un pedido en "En Caja" no tiene botón para avanzar: no se puede mandar a cocina un pedido take away sin cobrar. Según cómo eligió pagar el cliente, la tarjeta muestra "Aguardando selección de pago" (todavía no eligió), "MP — Aguardando confirmación de pago" con el botón "Refrescar Estado MP" (eligió MercadoPago), o el botón "Confirmar pago en efectivo" (eligió efectivo). Los pedidos de mesa nunca aparecen en "En Caja".

### 6.3 Qué ve el cliente take away en cada estado

En ProTable, la pantalla de seguimiento del pedido take away muestra un solo estado, aunque el cliente haya hecho más de un pedido. Estos son los textos que ve:

| Situación | Texto que ve el cliente |
|---|---|
| El pago todavía no se confirmó | "Esperando confirmación de pago en caja" |
| Pendiente | "Pedido recibido, en espera" |
| En preparación | "En preparación" |
| Listo | "Listo para entregar!" |
| Entregado | "Entregado. Gracias!" |

## 7. Pago y checkout

### 7.1 Medios de pago

En ProTable, el cliente elige el medio de pago en la pantalla de pago. Si intenta pagar sin elegir uno, ve el mensaje "Seleccioná un método de pago".

| Medio | Cómo se paga | A dónde va el dinero / qué tiene que hacer el local |
|---|---|---|
| MercadoPago | El cliente paga desde su celular: según la configuración del local, ProTable le muestra un código QR de MercadoPago en pantalla o lo lleva a MercadoPago para completar el pago | El dinero va a la cuenta de MercadoPago del local, que el dueño conecta desde el panel. El pago se registra solo cuando MercadoPago lo confirma; el local no tiene que confirmarlo a mano |
| Efectivo | El cliente indica que va a pagar en efectivo y el pago queda pendiente. En take away ve el mensaje "Tu pedido es el #N. Acercate a la caja para pagar." | El dinero lo recibe el personal del local. El mozo o la caja tienen que confirmar el cobro desde el tablero Kanban, desde la sección Pagos o desde la mesa. Hasta que lo confirman, el saldo de la cuenta no baja |

### 7.2 Pago con MercadoPago

En ProTable, cuando el cliente elige MercadoPago, el sistema genera el cobro por el monto que corresponde a su parte, más la propina si eligió dejar una. Según la configuración del local, el cliente ve un código QR de MercadoPago en pantalla o es redirigido a MercadoPago para pagar. El pago se registra en la cuenta del local cuando MercadoPago lo aprueba. Si MercadoPago rechaza el pago, el cliente ve el mensaje "Pago rechazado" y el saldo de la cuenta no cambia. Cuando el pago se aprueba, el cliente de mesa vuelve a la pantalla de sus pedidos y el cliente take away pasa a la pantalla de seguimiento de su pedido.

### 7.3 Vuelta de MercadoPago y comprobante

En ProTable, cuando el cliente paga en MercadoPago y vuelve a la app, llega a una pantalla de estado del pago. Esa pantalla recupera la cuenta del cliente a partir de los datos que devuelve MercadoPago, así que funciona aunque el celular haya perdido la información de la página al pasar por la app de MercadoPago. La pantalla muestra un comprobante con los productos consumidos. Si el pago quedó aprobado y el pedido es take away, a los pocos segundos pasa sola a la pantalla de seguimiento del pedido.

### 7.4 Pago en efectivo: lo confirma el personal

En ProTable, cuando un cliente elige pagar en efectivo, ya sea en la mesa o en take away, el pago queda pendiente y la cuenta sigue mostrando saldo. El cobro lo confirma el mozo o la caja, no el cliente. El personal puede confirmarlo desde el tablero Kanban (botón "Confirmar efectivo $X" en las tarjetas de una mesa, o "Confirmar pago en efectivo" en la columna "En Caja" para take away), desde la sección Pagos del panel o desde el detalle de la mesa. Al confirmar, el sistema descuenta el monto del saldo, sin superar lo que falta pagar. Si con ese pago la cuenta de la mesa queda saldada, la mesa se cierra sola.

### 7.5 Rechazar un pago en efectivo

En ProTable, si un cliente declaró un pago en efectivo pero el dinero no entró, el personal puede rechazarlo desde la sección Mesas o desde la sección Pagos del panel. El pago rechazado queda descartado y la deuda de la mesa no cambia. Además, cuando se cierra una mesa, los pagos en efectivo que hayan quedado pendientes se descartan solos.

### 7.6 Propina

En ProTable, la propina es opcional y la elige cada cliente al pagar su parte. Puede elegir 10 %, 15 % o 20 %, o escribir un monto propio; si vuelve a tocar el porcentaje que ya eligió, lo desactiva. El porcentaje se calcula sobre la parte que paga ese cliente, no sobre el total de la mesa. La propina se registra aparte y nunca descuenta la deuda de la mesa: lo que se cobra es la parte del cliente más la propina, y a la cuenta solo se le descuenta la parte.

## 8. Dividir la cuenta

### 8.1 Quién puede dividir la cuenta

En ProTable, dividir la cuenta está disponible para los pedidos en mesa, desde la pantalla de pago. Cada comensal elige si paga el total o una parte, y cómo calcula su parte. En los pedidos take away no se puede dividir: el cliente paga el total.

### 8.2 Modos de dividir la cuenta

En ProTable, el comensal que paga una parte elige uno de estos modos:

| Modo | Cómo funciona | Ejemplo |
|---|---|---|
| Pago total | El comensal paga todo el saldo pendiente de la mesa | La mesa debe $4.000 y un comensal paga los $4.000 |
| Partes iguales | El comensal elige entre cuántas personas se divide y qué número de persona es ("Persona X de N"). La parte se calcula sobre el total de la cuenta, redondeada hacia arriba | Cuenta de $4.000 entre 4: cada parte es $1.000 siempre |
| Por ítems | El comensal marca en una lista los productos que va a pagar, de todos los pedidos de la mesa, y paga la suma de esos productos | Un comensal marca solo los productos que consumió él y paga la suma |
| Monto personalizado | El comensal elige cuánto pagar con un control deslizante o escribiendo el monto | Un comensal decide pagar un monto fijo a cuenta del total |

### 8.3 Reglas al dividir la cuenta

En ProTable, las partes iguales se calculan sobre el total de la cuenta, no sobre lo que falta pagar, y cada pago se descuenta del total. Nadie puede pagar más que el saldo pendiente: si la parte calculada (por redondeo o por mezclar modos) supera lo que falta, se cobra solo el saldo. En el modo por ítems, si llegan pedidos nuevos mientras un comensal está eligiendo qué paga, la selección que ya hizo se conserva. La propina de cada comensal se suma a su parte y no descuenta la deuda de la mesa.

### 8.4 Monto personalizado y el mínimo de $1.000

En ProTable, en el modo de monto personalizado el control deslizante arranca en $1.000 como mínimo. Si el saldo pendiente de la mesa es menor a $1.000, el control deslizante se oculta y queda solo el campo para escribir el monto. En todos los casos el monto no puede superar el saldo pendiente.

### 8.5 Cuándo se cierra la mesa al pagar por partes

En ProTable, la cuenta de la mesa se va descontando con cada pago confirmado. Cuando la mesa queda totalmente paga, se cierra sola. Los pagos con MercadoPago se descuentan cuando MercadoPago los aprueba; los pagos en efectivo se descuentan recién cuando el personal los confirma.

## 9. Seguimiento del pedido por el cliente

### 9.1 Seguimiento en la mesa

En ProTable, el cliente de una mesa sigue sus pedidos en la pantalla de pedidos de la mesa. Esa pantalla no muestra "pedido 1, pedido 2", sino todos los productos agrupados por estado (pendiente, en preparación, listo, entregado, cancelado), sumando cantidades de un mismo producto. Arriba muestra el resumen de la mesa: cubiertos (si el local los cobra), total consumido, pagado y pendiente, con el botón "Pagar cuenta". Cuando la cuenta está pagada, el resumen se reemplaza por una pantalla de agradecimiento con el detalle final.

### 9.2 Seguimiento de un pedido take away

En ProTable, el cliente take away tiene una pantalla de seguimiento propia, con el logo y el nombre del local, su número de pedido y el estado actual. Si el cliente hizo más de un pedido, la pantalla muestra un solo estado combinado, priorizando lo más avanzado (por ejemplo, si algo está listo, muestra "Listo para entregar!"). La pantalla se actualiza sola en tiempo real y, como respaldo, vuelve a consultar el estado cada 10 segundos. Tiene un botón para compartir que copia el link de seguimiento.

### 9.3 Buscar un pedido take away por número o teléfono

En ProTable, si el cliente take away cerró la pantalla de seguimiento, puede buscar su pedido en el buscador público de pedidos, ingresando el número de pedido o el teléfono que dejó. Si el pedido está activo, el buscador lo lleva a la pantalla de seguimiento. Si el pedido ya terminó, muestra "El pedido #N fue completado el" seguido de la fecha y hora. Si no encuentra nada, muestra "No encontramos ningún pedido con ese número o teléfono".

### 9.4 Aviso cuando el pedido take away está listo

En ProTable, cuando un pedido take away pasa a Listo, el celular del cliente avisa con sonido, vibración y notificación. El aviso se dispara desde la pantalla de seguimiento del pedido.

## 10. Tablero Kanban del panel

### 10.1 Columnas del tablero Kanban

En ProTable, el tablero Kanban del panel muestra los pedidos del local en cinco columnas: "En Caja", "Pendientes", "En preparación", "Listos" y "Entregados". "En Caja" agrupa los pedidos take away que todavía no están pagados. Los pedidos cancelados no se muestran en el tablero. Los pedidos entregados se ven durante 24 horas y después desaparecen solos.

### 10.2 Temporizador con semáforo

En ProTable, cada tarjeta del tablero Kanban muestra un temporizador con colores de semáforo: verde de 0 a 5 minutos, amarillo de 5 a 10 minutos y rojo a partir de los 10 minutos. El tiempo se cuenta desde que se creó el pedido; en los pedidos entregados, se cuenta desde la entrega.

### 10.3 Alerta de alérgenos

En ProTable, la tarjeta del tablero Kanban muestra una alerta de alérgenos cuando la nota del pedido o la nota de algún producto menciona alguna de estas palabras: "sin tacc", "celíaco", "alergia", "alérgico", "sin gluten", "vegetariano", "vegano", "sin lactosa" o "diabético".

### 10.4 Avanzar y cancelar un pedido desde el tablero

En ProTable, cada tarjeta del tablero Kanban tiene un botón grande para pasar el pedido al estado siguiente: "Preparar" (de Pendiente a En preparación), "Listo" (de En preparación a Listo) y "Entregado" (de Listo a Entregado). Los pedidos en "En Caja" no tienen ese botón hasta que se confirma el pago. Desde la tarjeta también se puede cancelar el pedido, con confirmación, salvo que ya esté Entregado o Cancelado.

### 10.5 Cobros desde el tablero Kanban

En ProTable, el tablero Kanban permite confirmar cobros. En la columna "En Caja", si el cliente take away eligió efectivo, aparece el botón "Confirmar pago en efectivo"; si eligió MercadoPago, aparece el botón "Refrescar Estado MP" para consultar el pago en MercadoPago. En los pedidos de mesa, si algún comensal dejó un pago en efectivo pendiente, la tarjeta muestra el botón "Confirmar efectivo $X" con la suma pendiente. El monto que se confirma lo calcula el sistema.

### 10.6 Consulta automática de pagos de MercadoPago

En ProTable, el tablero Kanban consulta solo, cada 15 segundos, el estado de los pagos con MercadoPago de los pedidos take away que siguen esperando confirmación y se crearon en los últimos 30 minutos. Si MercadoPago informa que alguno se aprobó, el tablero se actualiza y el pedido sale de "En Caja". Para pedidos más viejos o para forzar la consulta, está el botón "Refrescar Estado MP" en la tarjeta.

### 10.7 Limpiar entregados

En ProTable, el tablero Kanban tiene un botón "Limpiar entregados" que archiva todos los pedidos entregados del local, con un paso de confirmación. El contador del botón muestra todos los entregados que se pueden archivar, no solo los que se ven en pantalla.

### 10.8 Vistas, filtros, pantalla completa y alertas sonoras

En ProTable, el tablero Kanban se puede ver de cuatro maneras (en columnas, en mosaico, dividido o en una vista de take away), y el tablero recuerda la vista elegida. Tiene un filtro por destino del pedido que, además, recalcula el total de cada pedido mostrando solo los productos de ese destino. También tiene modo de pantalla completa y alertas sonoras.

### 10.9 Lista de pedidos agrupada por mesa

En ProTable, además del tablero Kanban, el panel tiene una lista de pedidos agrupada por mesa, con el total y los productos de cada una. Arriba muestra cuántos pedidos hay pendientes, en preparación y listos. Se puede filtrar por destino (todos, cocina, bar u otro) y por estado. El filtro "activos" muestra los pedidos que no están ni entregados ni cancelados, y el filtro de entregados muestra solo los entregados del día.

## 11. Pantalla de cocina con PIN

### 11.1 Cómo ingresa la cocina

En ProTable, la cocina tiene una pantalla propia que no usa el usuario y la contraseña del panel. Para entrar se ingresa el código del restaurante (se escribe en mayúsculas) y un PIN numérico de 4 a 6 dígitos. Por seguridad, el sistema admite como máximo 5 intentos de ingreso cada 15 minutos por código de restaurante. Si en ese navegador ya hay una sesión de cocina abierta, la pantalla de ingreso lleva directo al tablero.

### 11.2 Cuánto dura la sesión de cocina

En ProTable, la sesión de la pantalla de cocina se guarda solo mientras el navegador está abierto: si se cierra el navegador, hay que volver a ingresar el código y el PIN. La pantalla tiene un botón para cerrar sesión. Si alguien intenta abrir el tablero de cocina sin haber ingresado, el sistema lo devuelve a la pantalla de ingreso.

### 11.3 Tablero de cocina

En ProTable, la pantalla de cocina muestra los pedidos en un tablero en columnas, igual al del panel. El tablero se actualiza solo cada 15 segundos. Tiene un filtro de destino con los botones Todos, Cocina y Bar, y arranca filtrado en Cocina. Desde ahí la cocina avanza los pedidos de estado. Los pedidos take away que están en "En Caja" no se pueden avanzar hasta que se confirma el pago. El tablero de cocina también tiene alertas sonoras y pantalla completa.

## 12. Mesas desde el panel

### 12.1 Abrir una mesa

En ProTable, el personal abre una mesa desde la sección Mesas del panel, en el detalle de la mesa. Al abrirla, la mesa queda ocupada y lista para que los clientes pidan escaneando el QR. Si la mesa ya tenía una cuenta activa, se sigue usando esa misma cuenta. Abrir la mesa es obligatorio para que el cliente pueda pedir: si no, ve "Mesa no disponible".

### 12.2 Cerrar una mesa

En ProTable, el personal cierra una mesa desde el detalle de la mesa en la sección Mesas. Al cerrarla, la mesa vuelve a quedar disponible y la cuenta se cierra. Los pagos en efectivo que hayan quedado pendientes de confirmar al momento del cierre se descartan solos. Además, cuando la cuenta de una mesa queda totalmente paga, la mesa se cierra sola sin que el personal tenga que hacerlo.

### 12.3 Cargar consumo a mano

En ProTable, el personal puede agregar productos a la cuenta de una mesa abierta desde el detalle de la mesa. Sirve para cargar un pedido que tomó el mozo, sin que el cliente lo pida por el QR. Lo cargado se suma a la cuenta de la mesa.

### 12.4 Cobrar en efectivo desde la mesa

En ProTable, el personal puede registrar un cobro en efectivo desde el detalle de la mesa, por el total o por una parte; el monto no puede superar el saldo. Si algún comensal ya dejó un pago en efectivo pendiente, el detalle de la mesa no ofrece cobrar: muestra "Hay un pago en efectivo pendiente de confirmar: $X" con los botones "Confirmar" y "Rechazar" para cada pago pendiente. El cobro se habilita de nuevo cuando no quedan pagos pendientes.

### 12.5 Códigos QR de las mesas

En ProTable, el QR de cada mesa se genera desde el detalle de la mesa en el panel. También hay una pantalla de códigos QR que imprime todos los QR de las mesas juntos en una hoja; esa pantalla está disponible cuando el local tiene habilitada la función de pedidos por QR. Cada QR apunta a una mesa en particular.

## 13. Cuenta de MercadoPago del local

### 13.1 Cómo se conecta la cuenta de MercadoPago

En ProTable, el local conecta su propia cuenta de MercadoPago desde la sección Configuración del panel, con el botón para conectar, o desde el paso de pagos del alta del local. Al conectar, el sistema lleva al dueño a MercadoPago para autorizar la conexión y después lo devuelve a ProTable. Solo el dueño de la cuenta del local puede conectar o desconectar MercadoPago. Al conectar la cuenta, ProTable desactiva el modo de solo efectivo del local.

### 13.2 A dónde va la plata de los pagos con MercadoPago

En ProTable, los pagos que hacen los clientes con MercadoPago se cobran con la cuenta de MercadoPago que conectó el local, así que el dinero va a esa cuenta. Es una cuenta distinta de la que usa ProTable para cobrarle el servicio al local. La propina que deja el cliente se cobra junto con su parte en el mismo pago.

### 13.3 Una cuenta de MercadoPago por local

En ProTable, una misma cuenta de MercadoPago no se puede vincular a dos locales distintos. Si el dueño intenta conectar una cuenta que ya está vinculada a otro local, el sistema no la conecta y muestra el mensaje "Esta cuenta de MercadoPago ya está vinculada a otra cuenta activa".

### 13.4 Qué pasa si el local no conectó MercadoPago

En ProTable, para cobrar con MercadoPago el local tiene que tener su cuenta de MercadoPago conectada. El sistema no usa ninguna cuenta alternativa: si el local no conectó la suya, no se puede generar el cobro con MercadoPago. La cuenta conectada se puede desconectar desde la sección Configuración.

### 13.5 Cómo se confirma un pago de MercadoPago

En ProTable, el pago con MercadoPago se confirma solo: cuando MercadoPago aprueba el pago, avisa al sistema, que descuenta el monto de la cuenta y, en take away, pasa el pedido a Pendiente para que entre a cocina. El local no tiene que confirmarlo a mano. Si ese aviso de MercadoPago no llega, el sistema puede recuperar el pago consultando directamente a MercadoPago: lo hace solo el tablero Kanban para los take away recientes, y el personal puede forzarlo con el botón "Refrescar Estado MP" de la tarjeta.

## 14. Problemas frecuentes y qué hacer

### 14.1 El cliente ve "Mesa no disponible"

En ProTable, el mensaje "Mesa no disponible" aparece cuando el cliente escanea el QR de una mesa que el personal no abrió. Qué hacer: abrir la mesa desde la sección Mesas del panel y pedirle al cliente que vuelva a escanear el QR.

### 14.2 El cliente ve "Mesa no encontrada"

En ProTable, el mensaje "Mesa no encontrada" aparece cuando la mesa del QR o del identificador ingresado no existe, o cuando no se pudo cargar. Qué hacer: verificar en la sección Mesas del panel que la mesa exista y que el QR impreso sea el que el panel genera para esa mesa. Si la mesa existe, pedirle al cliente que vuelva a escanear.

### 14.3 El cliente ve "No se pudo identificar el restaurante de esta mesa"

En ProTable, el mensaje "No se pudo identificar el restaurante de esta mesa. Volvé a escanear el QR." aparece cuando, al confirmar el pedido, el sistema no logra identificar a qué local pertenece la mesa. Qué hacer: pedirle al cliente que vuelva a escanear el QR de la mesa y confirme el pedido de nuevo.

### 14.4 Al cliente se le vació el carrito

En ProTable, el carrito se guarda solo mientras la página está abierta: si el cliente recarga la página antes de confirmar, pierde los productos del carrito. Qué hacer: el cliente tiene que volver a agregar los productos; la mesa se conserva y no hace falta volver a escanear.

### 14.5 Un pedido take away está en "En Caja" y no se puede avanzar

En ProTable, un pedido take away queda en la columna "En Caja" del tablero Kanban, sin botón para avanzar, mientras su pago no está confirmado. Qué hacer: si el cliente paga en efectivo, cobrar y tocar "Confirmar pago en efectivo" en la tarjeta. Si la tarjeta dice "Aguardando selección de pago", el cliente todavía no eligió cómo pagar.

### 14.6 El cliente pagó con MercadoPago pero el pedido sigue en "En Caja"

En ProTable, el pago con MercadoPago se confirma cuando llega el aviso de MercadoPago, y ese aviso a veces puede no llegar. Qué hacer: tocar "Refrescar Estado MP" en la tarjeta del pedido; el sistema consulta el pago directamente en MercadoPago y, si está aprobado, lo registra y pasa el pedido a Pendiente. El tablero también hace esta consulta solo para los take away de los últimos 30 minutos.

### 14.7 El cliente pagó en efectivo pero la mesa sigue con saldo

En ProTable, un pago en efectivo queda pendiente hasta que el personal lo confirma, y mientras tanto la cuenta sigue mostrando saldo. Qué hacer: confirmar el pago desde el tablero Kanban ("Confirmar efectivo $X"), desde la sección Pagos o desde el detalle de la mesa. Si el dinero no entró, rechazar el pago desde Mesas o Pagos; la deuda no cambia.

### 14.8 No se puede cobrar en efectivo desde el detalle de la mesa

En ProTable, el detalle de la mesa no ofrece cobrar en efectivo mientras haya un pago en efectivo de un comensal pendiente de confirmar; en su lugar muestra "Hay un pago en efectivo pendiente de confirmar: $X". Qué hacer: confirmar o rechazar cada pago pendiente; cuando no quedan pendientes, se habilita el cobro.

### 14.9 El cliente ve "Pago rechazado"

En ProTable, el mensaje "Pago rechazado" aparece cuando MercadoPago no aprobó el pago del cliente. El pago no se registra y el saldo de la cuenta no cambia. Qué hacer: el cliente tiene que volver a pagar su parte.

### 14.10 El cliente ve "Seleccioná un método de pago"

En ProTable, el mensaje "Seleccioná un método de pago" aparece cuando el cliente intenta pagar sin haber elegido MercadoPago o efectivo. Qué hacer: elegir un medio de pago y volver a tocar pagar. En take away, también hay que elegir el tipo de entrega antes de pagar.

### 14.11 El cliente take away no encuentra su pedido

En ProTable, el buscador de pedidos take away muestra "No encontramos ningún pedido con ese número o teléfono" cuando no hay ningún pedido take away con ese dato. Qué hacer: revisar que el cliente haya escrito bien el número de pedido o el mismo teléfono que dejó al identificarse. Si el pedido ya terminó, el buscador no lo abre: muestra que fue completado y la fecha y hora.

### 14.12 El link de take away no muestra el menú

En ProTable, el link de take away no muestra el menú cuando el link no corresponde a ningún local o cuando el local no tiene el take away habilitado. Si el problema es de conexión, la pantalla ofrece el botón "Reintentar". Qué hacer: verificar que el link sea el correcto del local y que el take away esté habilitado; ante un error de conexión, tocar "Reintentar".

### 14.13 Los pedidos entregados desaparecieron del tablero Kanban

En ProTable, el tablero Kanban muestra los pedidos entregados solo durante 24 horas, y el botón "Limpiar entregados" los archiva antes. Qué hacer: para ver los entregados del día, usar la lista de pedidos del panel con el filtro de entregados.

### 14.14 La cocina tiene que volver a ingresar el PIN

En ProTable, la sesión de la pantalla de cocina se pierde al cerrar el navegador. Qué hacer: volver a ingresar el código del restaurante y el PIN. El sistema admite como máximo 5 intentos de ingreso cada 15 minutos por código de restaurante, así que conviene revisar bien el código y el PIN antes de reintentar.

### 14.15 No se puede conectar la cuenta de MercadoPago

En ProTable, si al conectar MercadoPago aparece el mensaje "Esta cuenta de MercadoPago ya está vinculada a otra cuenta activa", es porque esa cuenta ya está conectada a otro local. Qué hacer: conectar una cuenta de MercadoPago distinta. Además, solo el dueño de la cuenta del local puede conectar MercadoPago.
## 15. Contacto y canales de soporte

### 15.1 Canales oficiales de soporte de ProTable

| Canal | Cómo se usa |
|---|---|
| Email | contacto@protable.io |
| WhatsApp | Canal oficial de soporte de ProTable |
| Centro de Ayuda | Guías paso a paso dentro del panel del local |

### 15.2 Soporte prioritario

El plan Pro de ProTable incluye soporte prioritario. El plan Enterprise incluye un responsable de cuenta dedicado.

### 15.3 Qué información conviene tener a mano al pedir ayuda

Al contactar al soporte de ProTable, conviene indicar el nombre del local, qué se estaba haciendo cuando apareció el problema, el mensaje exacto que se ve en pantalla y si el problema afecta a una mesa, a un pedido take away o al panel.
