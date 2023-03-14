FROM tensorflow/tensorflow:2.10.1-gpu-jupyter

WORKDIR /work

COPY requirements.txt requirements.txt

RUN apt-get update && apt-get install libgl1 nodejs -y

RUN pip install -r requirements.txt

EXPOSE 8888

ENTRYPOINT ["jupyter", "lab","--ip=0.0.0.0","--allow-root","--no-browser"]

