# Asignacion Automatica

Automatizacion de la Asignacion de solicitudes de pedido de SAP. La automatizacion sera hecha a los materiales, y esta representado con el siguiente diagrama:


![WhatsApp Image 2022-05-09 at 1 09 12 PM](https://user-images.githubusercontent.com/91348491/167451972-e6277d96-3ca0-49fa-bbc0-0122f13ca2d7.jpeg)

## Transaccion Me5a
Tomaremos los datos de esta transaccion y para luego pasar a la transaccion a la ZAR_BEDNR_UPD. Lo que no haremos es hacer una descarga automatica, mas bien, leer los valores de Sap y pasarlos a Excel para tenerlos durante la ejecucion del programa. 
Haremos el siguiente filtrado:
* Solicitudes con SKU (Con codigo de material)
* Solicitudes sin asignacion (Campo Req. Tracking Number vacio) y solicitudes con asignacion "BERGATINO"

Entonces los datos que tomaremos en el excel sera:

| Req. Tracking Number | Solicitud de Pedido | Posicion | Centro | Material |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| BERGATINO  | 10994596 | 10  | 2805  | 10.245.155  |
|   | 10942556 | 10  | 1270  | 10.558.233  |

