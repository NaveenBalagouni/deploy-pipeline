# Your app Dockerfile (e.g., for a Python app)
FROM python:3.8-slim

WORKDIR /app

COPY . .

RUN pip install -r requirements.txt

CMD ["python", "app.py"]
