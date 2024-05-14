### 1. Crea un objeto DEPLOYMENT con las siguientes caracteristicas:
- Nombre: "demogato" 
- Imagen: tomcat
- Créalo de manera IMPERATIVA.

```
kubectl create deployment demogato --image=tomcat
```
![alt text](image.png)
---

### 2. Lista los POD.

```
kubectl get pods
```
![alt text](image-1.png)
 - Esperamos un poco a ue esté en Running
 
![alt text](image-2.png)

### 3. Lista los DEPLOYMENT.
```
kubectl get deployments
```
![alt text](image-3.png)
 - Esperamos un poco a ue esté en Ready

![alt text](image-4.png)
### 4. Borra el DEPLOYMENT.
```
kubectl delete deployment demogato
```
![alt text](image-5.png)


### 4. Lista los POD.
```
kubectl get pods
```
![alt text](image-6.png)