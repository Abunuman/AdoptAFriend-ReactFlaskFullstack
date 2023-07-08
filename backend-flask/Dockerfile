FROM python:3.10-slim-buster

# Inside Container
# make a new folder inside the container
WORKDIR /backend-flask

# This contains the libraries we want to install
COPY requirements.txt requirements.txt

# Install the python libraries used for the app
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

RUN apt-get update && apt-get install -y curl

CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0" "--port=4567"]

