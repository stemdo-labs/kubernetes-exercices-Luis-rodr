### 1. Crea un POD con las siguientes características:
   - Nombre "apache"
   - Imagen httpd
   - Hazlo de manera IMPERATIVA.

```
kubectl run apache --image=httpd
```

![alt text](\images\image.png)
---

### 2. Lista los POD.
```
kubectl get pods
```
![alt text](\images\image-1.png)

### 3. Describe el POD.
```
kubectl describe pod apache
```
![alt text](\images\image-3.png)
![alt text](\images\image-4.png)

### 4. Borra el POD.

```
kubectl delete pod apache
```
![alt text](\images\image-2.png)