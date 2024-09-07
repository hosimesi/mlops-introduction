FROM python:3.12-slim AS base

# Update and install dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    gcc \
    git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /app
ENV PYTHONPATH=/app

COPY pyproject.toml poetry.lock ./

# Install poetry and export dependencies
RUN pip install --upgrade pip \
    && pip install poetry=="1.8.3" \
    && poetry export --with app --without-hashes -f requirements.txt -o requirements.txt \
    && pip install -r requirements.txt

COPY train.ipynb /app
