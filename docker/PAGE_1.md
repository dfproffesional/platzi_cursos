
### Modo Interactivo
En este ejemplo se intento ejecutar ``docker run alpine `` pero no tuvo exito en su ejecucion ya que su status es ``exited (0)``, es decir, culmino.
**Nota:** Cualquier codigo diferente de cero significa que hubo un error.
![Image PS](./.src/capture_dk_ps.png)
**Porque ocurrio?** Esto ocurre, debido a que el comando por defecto que se utilizo fue el shell. Por lo que ejecuto y cerro todo.
Probemos usando ``it``, ``docker run -it alpine``
![Image Alpine](./.src/capture_dk_alpine.png)
Como puedes observar se libera el comand prompt del contendor, pero al salir nuevamente este proceso culmina.

#### Ciclo de Vida de un Contenedor
La explicacion por la cual un contenedor se detiene luego de acceder usando un interprete es porque su main process ```/bin/bash``` ya se ejecuto pero sin ninguna otra entrada por lo que inicio y termino.
Para evitar esto debemos proporcionar un comando diferente para que se mantenga en ejecucion.
Ejemplo:
``docker run --name example2 -d alpine tail -f /dev/null``
![Image Alpine](./.src/capture_dk_alpine_2.png)
![Image Alpine](./.src/capture_dk_alpine_ps.png)
Para inspeccionar que proceso especifico esta ejecutando este contenedor se puede usar lo siguiente:
``docker inspect --format '{{.State.Pid}}' example2``
Para Eliminarlo
``kill -9 (PID obtenido)``
### Exponiendo Contenedores
