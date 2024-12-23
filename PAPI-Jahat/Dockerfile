FROM python:3.10

RUN mkdir /home/papi-jahat

WORKDIR /home/papi-jahat

COPY ./requirements.txt .

RUN pip install -r requirements.txt

COPY ./src /home/papi-jahat

CMD ["fastapi","run","main.py"]
