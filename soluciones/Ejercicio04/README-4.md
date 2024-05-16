### 1. Crea un objeto DEPLOYMENT con las siguientes caracteristicas:
- Nombre: "demogato" 
- Imagen: tomcat
- Créalo de manera IMPERATIVA.

```
kubectl create deployment demogato --image=tomcat
```
![alt text](\images\image.png)
---

### 2. Lista los POD.

```
kubectl get pods
```
![alt text](\images\image-1.png)
 - Esperamos un poco a ue esté en Running
 
![alt text](\images\image-2.png)

### 3. Lista los DEPLOYMENT.
```
kubectl get deployments
```
![alt text](\images\image-3.png)
 - Esperamos un poco a ue esté en Ready

![alt text](\images\image-4.png)
### 4. Borra el DEPLOYMENT.
```
kubectl delete deployment demogato
```
![alt text](\images\image-5.png)


### 4. Lista los POD.
```
kubectl get pods
```
![alt text](\images\image-6.png)