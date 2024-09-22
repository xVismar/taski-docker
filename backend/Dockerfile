FROM python:3.9

RUN pip install --upgrade pip

COPY ./requirements.txt .
RUN pip install -r requirements.txt

COPY . /app
WORKDIR /app


CMD ["gunicorn", "backend.wsgi:application", "--bind", "0.0.0.0:8000"]