FROM python:3.11-slim

WORKDIR /app

COPY docker/db-setup/requirements.txt .


RUN pip install -r requirements.txt
RUN apt-get update

COPY utils.py .
COPY docker/db-setup/db-init.py .

CMD ["python", "db-init.py "]