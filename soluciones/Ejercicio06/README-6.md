### 1. Usando el ejercicio anterior, escala la aplicación de  tres maneras diferentes, aumentando 1, 2 y 3 réplicas respectivamente.
 1. De forma declarativa, mediante la edición del manifiesto YAML, y utilizando `kubectl apply -f <nombre_archivo>`
    ```yaml
    ...
    spec:
      replicas: 2 # Añado solo una réplica
      selector:
        matchLabels:
    ...
    ```
    ```console
    kubectl apply -f demo-gat.yaml
    ```
    ![alt text](images\image.png)

 1. De forma Imperativa, con `kubectl scale <resource-kind> <resource-name> --<option>=<value>` 
    ```bash
    kubectl scale deploy demogat-yaml --replicas=3
    ```
    ![alt text](images\image-1.png)


 1. De forma imperativa, e interactiva, con `kubectl edit <resource-kind> <resource-name>`
    ```bash
    kubectl edit deploy demogat-yaml
    ```
    ![alt text](images\image-2.png)
    ![alt text](images\image-3.png)

### 2. Borra el DEPLOYMENT.
    ```bash
        kubectl delete deploy demogat-yaml
    ```
![alt text](images\image-4.png)