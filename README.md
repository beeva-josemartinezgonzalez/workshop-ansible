# [genDevOps] workshop-ansible

El propósito de este ejercicio es poner en práctica los recursos esenciales de 
Ansible que hemos visto, desplegando una serie de servicios sobre tres servidores.

El stack se compone de un **proxy**, un **backend** tonto y una aplicación de **monitoring**.

En este repo se encuentra la estructura básica del proyecto, con ciertos ficheros a medio 
configurar y diversas pistas, con todos los ficheros accesorios necesarios ya definidos.

Cada equipo dispondrá de un entorno aislado, con keys dedicadas y dns para probar :D. 

## Parte 1

Provisionar la máquina de proxy.

## Parte 2

Provisionar la máquina de backend.  

Para probar que funciona correctamente bastará con una petición GET con curl o 
acceder con el navegador a `http://proxy/` o `http://proxy/hi/name` 

[grumpy](https://github.com/ivanfoo/grumpy)

## Parte 3

Desplegar la aplicación de monitoring en la máquina de proxy. Se puede comprobar 
su funcionamiento accediendo a `http://proxy:8000/metrics`

[meter](https://github.com/ivanfoo/meter)

## Tips

El proxy escucha por el puerto 80, redireccionando las peticiones a los servidores 
de backend, que estarán escuchando en el puerto 8080.   

Para la parte final, se incluye una config extra para que el proxy acepte peticiones 
en el puerto 8000 y las rediriga al 3000, donde esta desplegado el servicio de monitoring.

