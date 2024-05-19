## Ejercicio 11 pero con la estrategia 'Recreate'

### 1. Crea un namespace con el nombre que prefieras.

`kubectl create namespace ej12`

![alt text](image.png)

### 2. Tomaremos el deployment del ejercicio 5 y lo modificaremos para que use la estrategia RollingUpdate.

Añado:


![alt text](image-1.png)

(El campo replicas es opcional, siendo que el default es 1)
### 3. Despliega el deployment en el namespace creado.

`kubectl apply -f demo-gat.yaml`

![alt text](image-2.png)

### 4. Modifica el deployment para usar una tag diferente de la imagen.

Usaremos la imagen `tomcat:10.1-jre21-temurin-jammy`

### 5. Actualiza el deployment para que use la nueva imagen.

`kubectl apply -f demo-gat.yaml`

![alt text](image-3.png)

### 6. Explica el proceso de actualización de la imagen.

Aquí, primero borra todo y después lo crea desde cero.
Esto implica que para estructuras más complejas habrá un tiempo mayor en el que los pods no estén creados

### 7. Limpia todos los recursos creados.

En lugar de borrar en orden, deployment, service y demás, en este caso opto por usar `kubectl delete namespace ej12

Esto tiene relativamente el mismo efecto.