FROM python:3.7-slim

ENV PYTHONUNBUFFERED=1

WORKDIR /app

COPY Pipfile Pipfile.lock ./

RUN pip install pipenv \
 && pipenv install --system
