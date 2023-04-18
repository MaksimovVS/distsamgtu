FROM python:3.10-slim

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY requirements.txt .

RUN pip3 install --upgrade pip && pip3 install -r requirements.txt --no-cache-dir

COPY . .

ENTRYPOINT ["gunicorn", "samgtudist.wsgi:application", "--bind", "0.0.0.0:8000" ]