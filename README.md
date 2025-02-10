# Final Assingment of Machine Learning with Big Data course

This report constitutes the final assignment for the Machine Learning with Big Data course. It focuses on analyzing the FIFA 18 dataset. Four types of analysis are conducted: classification, regression, clustering, and anomaly detection. To perform these analyses, data preprocessing, including cleaning, noise handling, and normalization are performed. Then, supervised and unsupervised learning algorithms are employed, such as neural networks and k-means, for the analysis. In addition, other techniques are utilized to improve the accuracy of the analysis, including PCA for dimensionality reduction and the Elbow method for determining the optimal number of clusters in K-means. The results were evaluated using various metrics such as F1-score, MSE, RMSE, and correlations.

### To run the codes using a Kubernetes cluster, follow these instructions:

Navigate to the project directory.
```bash
cd project
```
Build the Docker image and run the docker container locally to test.
```bash
docker build -t jupyter-implementations .
docker run -p 8888:8888 jupyter-implementations
```

Jupyter Notebook can be accessed at `http://localhost:8888` in local browser.
Tag the image, log in to Docker hub, and push the image.
```bash
docker tag jupyter-implementations <dockerhub-username>/jupyter-implementations:latest
docker login
docker push <dockerhub-username>/jupyter-implementations:latest
```
Apply the YAML files for deployment.
```bash
kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get services
```
Use NodePort to access the notebook.
For example: `http://<external-ip>:80/`

### To run the code in a local machine, follow these instructions:
Install all requirements.
```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow
```
Run `Implementations.ipynb` using a IDE.
