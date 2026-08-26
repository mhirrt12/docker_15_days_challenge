FROM python:3.13

WORKDIR /app

RUN pip install  requests
EXPOSE 8000
COPY . .

CMD ["python", "app.py"]