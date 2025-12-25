FROM python:3.12

WORKDIR /app

RUN pip install gunicorn==23.0.0

COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir

COPY . .

CMD ["gunicorn", "backend.wsgi:application", "--bind", "0.0.0.0:8000"]
