### Crear ConfigMap

Creo primero un namespace ara todo el 'proyecto'

`kubectl apply -f namespace.yaml`

![alt text](image.png)

Luego creo el configMap

`kubectl create configmap ej-13-configmap --from-file ./index.html -n ej13`

![alt text](image-1.png)

### Crea tanto un deployment como un service, que muestre el contenido del ConfigMap desde un navegador.

`kubectl apply -f service.yaml`

![alt text](image-5.png)

Uso una imagen de nginx

`kubectl apply -f deploy.yaml`

![alt text](image-4.png)

`kubectl get all -n ej13 -o wide`
![alt text](image-3.png)

`minikube service app-service -n ej13 `
![alt text](image-2.png)