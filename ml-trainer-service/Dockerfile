FROM python:3.10-slim

WORKDIR /app

COPY main.py /app/
COPY preprocess.py /app/
COPY training.py /app/
COPY utils.py /app/
COPY requirements.txt /app/
COPY training_data.csv /app/

RUN pip3 install --no-cache-dir -r requirements.txt

VOLUME ["/model-storage"]

EXPOSE 8002

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8002"]
