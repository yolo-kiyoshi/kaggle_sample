FROM python:3.7-slim

ENV PYTHONUNBUFFERED=1

WORKDIR /app

RUN apt-get update \
   && apt-get install libgomp1

COPY poetry.lock pyproject.toml ./

RUN pip install poetry

RUN poetry config virtualenvs.create false \
  && poetry install