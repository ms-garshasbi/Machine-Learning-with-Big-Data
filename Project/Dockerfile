FROM jupyter/base-notebook
WORKDIR /home/jovyan/work
COPY Implementations.ipynb /home/jovyan/work/
COPY requirements.txt /home/jovyan/work/
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 8888
CMD ["start-notebook.sh", "--NotebookApp.token=''", "--NotebookApp.password=''"]
