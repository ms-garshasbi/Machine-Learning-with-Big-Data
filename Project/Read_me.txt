To run the codes using a Kubernetes cluster, follow these instructions:

#Navigate to the project directory
cd project

#Build the Docker image and run the docker container locally to test
docker build -t jupyter-implementations .
docker run -p 8888:8888 jupyter-implementations

#Jupyter Notebook can be accessed at http://localhost:8888 in local browser.

#Tag the image, log in to Docker hub, and push the image
docker tag jupyter-implementations <dockerhub-username>/jupyter-implementations:latest
docker login
docker push <dockerhub-username>/jupyter-implementations:latest

#Apply the YAML files for deployment
kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get services

#use NodePort to access the notebook.
#For example: http://<external-ip>:80/

###############################
To run the code in a local machine, follow these instructions:

#Install all requirements
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow

#Run Implementations.ipynb using a IDE 

