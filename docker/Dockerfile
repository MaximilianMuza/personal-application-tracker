FROM python:3.10.3-slim-buster

WORKDIR /usr/src/app

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update

COPY . .
RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt && \
    rm requirements.txt

EXPOSE 8050

COPY src/ src/
WORKDIR /usr/src/app/src

CMD python main.py