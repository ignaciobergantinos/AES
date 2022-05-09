# Asignacion Automatica

Automatizacion de la Asignacion de solicitudes de pedido de SAP. La automatizacion sera hecha a los materiales, y esta representado con el siguiente diagrama:


![WhatsApp Image 2022-05-09 at 1 09 12 PM](https://user-images.githubusercontent.com/91348491/167451972-e6277d96-3ca0-49fa-bbc0-0122f13ca2d7.jpeg)

## Transaccion Me5a
Tomaremos los datos de esta transaccion, lo que no haremos es hacer una descarga automatica, mas bien, leer los valores de SAP y pasarlos a Excel para tenerlos durante la ejecucion del programa. 
Haremos el siguiente filtrado:
* Solicitudes con SKU (Con codigo de material)
* Solicitudes sin asignacion (Campo Req. Tracking Number vacio) y solicitudes con asignacion "BERGATINO"
* Centros que especificaremos

Entonces los datos que tomaremos en el excel sera:

| Req. Tracking Number | Solicitud de Pedido | Posicion | Centro | Material |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| BERGATINO  | 10994596 | 10  | 2805  | 10.245.155  |
|   | 10942556 | 10  | 1270  | 10.558.233  |

Para este paso, la primer parte del programa lo que hace es tomar 
![image](https://user-images.githubusercontent.com/91348491/167454711-6518c1bf-5256-4df7-b138-c8f50c5489f5.png)

### Referencias tomadas:

Nombre de transaccion:

![image](https://user-images.githubusercontent.com/91348491/167454961-e3b4ccf4-a566-4032-acbb-8b75cccebc2e.png)
Se coloca /n para que podamos ejecutar dicha transaccion dentro de otras transacciones.

Nombre_usuario y nombre_variante:

![image](https://user-images.githubusercontent.com/91348491/167455161-e9bf895d-1614-407b-8063-7d62342b6c26.png)

Nombre_layout: (tiene que ser exactamente igual)

![image](https://user-images.githubusercontent.com/91348491/167455214-c2ade708-8712-4c92-bb94-9bd9f7c42c56.png)


## Busqueda Historico
Una vez que tengamos los materiales a buscar, vamos hacer una busqueda de los materiales en una base de datos, en la que tendremos la categoria perteneciente a este material:
* Si encuentra historico --> Toma la categoria
* Si no encuentra --> Dependiendo el centro asigna a BERGATINO, o lo asigna a Manu Diaz (hablar con el, PENDIENTE).

## Busqueda Categoria
Una vez tengamos la 
