FROM python:3.9-slim

WORKDIR /app

COPY . /app
RUN apt-get update && apt-get install -y git && \
    git clone https://github.com/smartiqaorg/geometric_lib.git /app/geometric_lib

CMD ["python", "/app/main.py"]