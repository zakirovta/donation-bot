FROM python:3.8 AS builder
COPY requirements.txt .

RUN pip freeze > requirements.txt
RUN pip install --no-cache-dir -r requirements.txt
COPY ./src .

CMD [ "python", "-u", "./main.py" ]