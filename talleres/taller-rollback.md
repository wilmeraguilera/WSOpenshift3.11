
# Ejercicio de Rollback

Openshift tiene la posibilidad de realizar rollback de una aplicacion.  La manera de realizarlo es apartir 
del historial de configuraciones de despliegue.

El comando para ver los historiales del Deployment Config es el siguiente

``
oc rollout history dc/calculadora-spring
``
