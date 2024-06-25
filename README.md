# Resumen de utilización

## Para ejecutar las simulaciones en SUMO se deben seguir los siguientes pasos:

1. Desargar el programa de SUMO

2. Si tienes Windows, asegurarte de que el path de netconvert está agregado a tu computadora (Este paso en algunas compus es automático)
    En el caso de que no se haya hecho solo, solo debes meterte a [Ver la configuración avanzada del sistema->Variables de Entorno->Variables del sistema->buscas "Path"->Pones editar y 
    agregas el path de netconvert que se ubica en la carpeta de SUMO->Bins->netconvert.exe]

3. Descarga el conjunto de archivos de este mismo github, ya que la simulación se hace en base a los archivos anteriores.
3.1 Si deseas modificar la simulación es el momento (edges.xml, nodes.xml, routes.rou.xml, trafficLights.add.xml, mySimulation.sumocfg)

4. Para generar el archivo mynetwork.net.xml debes ejecutar en tu cmd ubicado en la carpeta de los archivos mencionados el siguiente código:
```
netconvert --node-files=nodes.xml --edge-files=edges.xml --output-file=mynetwork.net.xml
```
5. Para ejecutar la simulación, en el mismo cmd, en la misma ubicacion de archivos ejecuta el siguiente código:
```
sumo-gui -c mySimulation.sumocfg
```

> [!TIP]
>   1. Ponle un retardo si o si (Recomiendo 90).
>   2. Arriba a la izquierda se pone play.


## Resumen de la simulación:

### Explicación
Red Compleja: Red con cinco nodos, incluyendo un nodo con semáforo (n4).
Semáforos: Configurados correctamente para el nodo n4.
Rutas: Dos rutas (r1 y r2) definidas.
Vehículos: vehículos de distintos colores
