FROM python:3.9.3

RUN pip install --upgrade pip

RUN adduser -D myuser
USER myuser
WORKDIR /home/myuser

COPY --chown=myuser:myuser requirements.txt requirements.txt
RUN pip install --user -r requirements.txt
COPY --chown=myuser:myuser ./src .

CMD [ "python", "-u", "./main.py" ]