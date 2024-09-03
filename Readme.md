1. Create the image.
docker build -t myaksdemo.azurecr.io/web-game:tag <app>
2. login to ACR 
az acr login -n <ACRName>
3. push the image to ACR 
docker push myaksdemo.azurecr.io/web-game:tag
4. Deploy the image on AKS 
cd Kubernets
kubectl apply -f deploy.yml

Check the AKS and access the External Ip address.