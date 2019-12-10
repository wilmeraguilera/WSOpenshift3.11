# Config Map

A continuación se define un comando de ejemplo para la creación del config-map a partir de un archivo application.properties

```
oc create configmap map-app --from-file=application.properties 
```

Openshift tambien ofrece la posibilidad de crear configmaps a partir de literales (Pares clave valor), a continuación se muestra un ejemplo para crearlo a partir de literales.

```
oc create configmap map-app-var --from-literal SPRING_PROFILES_ACTIVE=qa
```


# Montar Config Map

Openshit tiene la posibilidad