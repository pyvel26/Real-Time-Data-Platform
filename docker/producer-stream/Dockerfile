FROM python:3.11-slim

WORKDIR /app

COPY docker/producer-stream/requirements.txt .

RUN pip install -r requirements.txt
RUN apt-get update && apt-get \
install -y procps

COPY utils.py .
COPY docker/producer-stream/producer.py .

CMD ["python", "producer.py"]
