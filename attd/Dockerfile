FROM python:3.11-slim-bullseye

RUN mkdir /home/attd

WORKDIR /home/attd

COPY ./requirements.txt .

RUN apt-get update && apt-get upgrade -y \
    && apt install python3-pip -y \
    && pip install -r requirements.txt

COPY ./src /home/attd/

CMD ["python3","./main.py"]