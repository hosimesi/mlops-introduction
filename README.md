# mlops-introduction
This Repository is used in the MLOps part of the CA 1Day Youth Boot Camp held on September 28, 2024 at CyberAgent.
[The first part](https://github.com/hosimesi/mlops-introduction/blob/main/1-notebook-in-docker) is an introduction to docker that puts the pre-created Notebook into docker.
[The second part](https://github.com/hosimesi/mlops-introduction/blob/main/2-docker-mlflow) is about experiment management using MLflow.

Slide: path to link

## Prerequisites
| Software         | Install (Mac)                |
| ---------------- | ---------------------------- |
| [Docker][docker] | `brew install --cask docker` |

[docker]: https://docs.docker.com/docker-for-mac/

## Get Started
### Setup environment
```bash
unzip train_data.zip
```

```bash
cp train_data 1-notebook-in-docker/train_data
```

```bash
cp train_data 2-docker-mlflow/train_data
```

## 1. [Notebook in Docker](1-notebook-in-docker)

```bash
$EDITOR Dockerfile
```

```bash
docker build . -t notebook-in-docker:1.0
```

```bash
docker run -p 8080:8080 --rm notebook-in-docker:1.0
```

## 2. [Docker MLflow](2-docker-mlflow)

```bash
$EDITOR compose.yaml
```

```bash
$EDITOR train.ipybn
```

```bash
docker compose up --build
```
