
# Ejercicio de Rollback

Openshift tiene la posibilidad de realizar rollback de una aplicacion.  La manera de realizarlo es apartir 
del historial de configuraciones de despliegue.

El comando para ver los historiales del Deployment Config es el siguiente

``
oc rollout history dc/calculadora-spring
``

``
[waguilera@localhost idea-pipeline-spring]$ oc rollout history dc/calculadora-spring
deploymentconfigs "calculadora-spring"
REVISION	STATUS		CAUSE
1		Failed		manual change
2		Complete	manual change
3		Complete	manual change
4		Complete	manual change
``

Si se desea realizar un rollback se debe indicar el numero de la revisión del deployment config y ejecutar el siguiente comando.

``
oc rollback <<deployment config>> --to-version=2
``
Ejemplo:
``
[waguilera@localhost idea-pipeline-spring]$ oc rollback dc/calculadora-spring --to-version=2
deploymentconfig.apps.openshift.io/calculadora-spring deployment #5 rolled back to calculadora-spring-2

``
