FROM python:3.13

WORKDIR /app

COPY requirements.txt .
EXPOSE 5173

RUN pip install -r requirements.txt

COPY . .

CMD ["python", "app.py"]