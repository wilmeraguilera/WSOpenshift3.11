# Config Map

A continuación se define un comando de ejemplo para la creación del config-map a partir de un archivo application.properties

```
oc create configmap map-app --from-file=application.properties 
```

# Delete