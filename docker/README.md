# Aprendiendo Docker
![Image Banner](./.src/dockerbanner.jpg)
## Primeros Pasos
### Que es?
Docker es un solucion tecnologica para aplicar una filosofia de contenedores; su objetivo principal es apoyar a nuestros equipos de trabajo en la **construccion, distrbucion y ejecucion de codigo o aplicaciones** de forma adecuada y asi no percibir errores en el proceso.

### Es una maquina Virtual?
Docker podria llegar a confundirse con una **maquina virtual** pero la realidad es que poseen **diferencias**. 
Una maquina virtual proporciona una **replica exacta de un ordenador**, Replica: hardware, software y dependencias llegando a un punto en el cual llega a ser muy pesado.
En cambio un sistema de **contenedores** reutiliza secciones del sistema para unicamente **virtualizar procesos**, de tal manera que la reduccion de espacio y consumo es alto.
![Image VM](./.src/docker_vs_vm.png)

### Arquitectura de Docker
Entre las principales cosas que debemos conocer de docker estan:

1. (Server) Docker daemon
2. REST API
3. docker cli
    - Container
    - Network
    - Image
    - Data Volume

### Comandos Basicos
Ejemplo: docker [OPTIONS] COMMAND

|commands|descriptions|
|--------|------------|
|ps      | Proporciona informacion de los contenedores en ejecucion|
|inspect | Proporciona informacion mas detallada del contenedor.
|run| Ejecuta un comando en un nuevo contenedor
|rm| Elimina un contenedor
|docker container prune | Borrar todos los containers apagados.|
|exec| Ejecutar un comando en un contenedor en ejecucion.|

[Siguiente](./PAGE_1.md)