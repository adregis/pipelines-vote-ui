FROM image-registry.openshift-image-registry.svc:5000/openshift/python:latest

# Instala as dependências primeiro para aproveitar o cache de camadas
ADD requirements.txt /opt/app-root/src/requirements.txt
RUN pip install -r /opt/app-root/src/requirements.txt

# Copia todo o conteúdo da pasta atual para o container
ADD . /opt/app-root/src

EXPOSE 8080

CMD ["python", "./app.py"]
