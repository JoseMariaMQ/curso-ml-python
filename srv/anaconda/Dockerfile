FROM continuumio/anaconda3

ADD ./srv/anaconda/conf/requirements.txt /

RUN apt-get update && apt-get -y install build-essential && pip install --upgrade setuptools && pip install -r requirements.txt
RUN mkdir -p /root/.jupyter
COPY ./srv/anaconda/conf/jupyter_notebook_config.json /root/.jupyter/jupyter_notebook_config.json
COPY ./srv/anaconda/datasets /opt/datasets

EXPOSE 8888
