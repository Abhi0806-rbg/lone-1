FROM python:3.10-slim

WORKDIR /app

# Copy files directly (no /app/ folder exists now)
COPY main.py /app/
COPY preprocess.py /app/
COPY requirements.txt /app/
COPY model.pkl /app/model/model.pkl

RUN pip3 install --no-cache-dir -r requirements.txt

EXPOSE 8001

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8001"]
