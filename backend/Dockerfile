FROM python:3.9

WORKDIR /app

RUN pip install --upgrade pip

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .


CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi:application"]
