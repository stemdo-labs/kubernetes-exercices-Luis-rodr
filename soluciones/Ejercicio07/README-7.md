### 1. Ejercicio vídeo 89
#### Generar despliegue y servicio
`docker build -t apasoft/web`
![alt text](images/image.png)

`kubectl apply completo.yaml`
![alt text](images/image-1.png)

`kubectl get pod`
![alt text](images/image-2.png)

`kubectl get svc`
![alt text](images/image-3.png)

`minikube service web-svc`
![alt text](images/image-4.png)

Y podemos acceder a:

![alt text](images/image-7.png)

Alternativamente, modificando el tipo de servicio, por ejemplo, en `Recursos/completo.yaml` y removiendo las referencias al tipo nodeport, por lo cual ponemos el tipo cluster-ip por default.

```yaml
apiVersion: v1
kind: Service
metadata:
  name: web-svc
  labels:
     app: web ##Puede ser otra etiqueta
spec:
  ports:
  - port: 80
    #nodePort: 30002  #Normalmente es aleatorio
    protocol: TCP
  selector:
     app: web
```
Y ejecutando
`kubectl port-forward web-d-65645dbbbc-xlwsv 9999:80`
![alt text](images/image-5.png)
Podemos acceder a
![alt text](images/image-6.png)