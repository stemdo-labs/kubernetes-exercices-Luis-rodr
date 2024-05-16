### 1. Crea un manifiesto de un POD con estas caracteristicas:
  - Nombre "apache-yaml"
  - Imagen *httpd* 
  - Incluye en este manifiesto los elementos necesarios para que cuente con una pólítica de reincio, para que *siempre* se reincie.
  - Despliégalo de manera DECLARATIVA.

```
kubectl apply -f .\apache-yaml.yaml
```

![alt text](\images\image.png)
---

### 2. Lista los POD mostrando toda la información posible.

```
kubectl get pods -o wide
```
![alt text](\images\image-1.png)

### 3. Conecta el puerto del POD a un puerto de tu equipo para poder acceder a él.
```
kubectl port-forward pod/apache-yaml 8080:80
```
![alt text](\images\image-3.png)
![alt text](\images\image-2.png)

### 4. Borrar el POD 
Primero salgo del comando anteior con Ctrl + C, luego, 
```
kubectl delete pod apache-yaml
```
![alt text](\images\image-5.png)