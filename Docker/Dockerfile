FROM python:3.9.3
COPY requirements.txt .

RUN pip freeze > requirements.txt
RUN pip install -r requirements.txt
COPY ./src .

CMD [ "python", "-u", "./main.py" ]