FROM ubuntu:latest

ENV FLASK_APP="backend/app.py"

RUN apt update
RUN apt install python3.11 python3-pip curl -y

RUN curl -sL https://aka.ms/InstallAzureCLIDeb | bash

RUN mkdir /backend

COPY ./backend /backend

RUN pip3 install -r ./backend/requirements.txt

EXPOSE 5000
CMD [ "flask", "run","--host","0.0.0.0","--port","5000"]