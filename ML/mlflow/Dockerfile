FROM python:3.10.12

WORKDIR /app
COPY requirements.txt /app/requirements.txt

RUN pip install -r /app/requirements.txt

COPY . .

EXPOSE 5500
