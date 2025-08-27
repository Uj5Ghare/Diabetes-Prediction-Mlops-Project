# 🩺 Diabetes Prediction Model – Your First MLOps Project (FastAPI + Docker + K8s + Helm + GitHub Actions)


This project helped me learn **Building and Deploying an ML Model** using a simple and real-world use case: predicting whether a person is diabetic based on health metrics. We’ll go from:

- ✅ Model Training
- ✅ Building the Model locally
- ✅ API Deployment with FastAPI
- ✅ Dockerization
- ✅ Kubernetes Deployment
- ✅ Helm Chart for Kubernetes Deployment
- ✅ GitHub Actions for CI/CD

---

## 📊 Problem Statement

Predict if a person is diabetic based on:
- Pregnancies
- Glucose
- Blood Pressure
- BMI
- Age

We use a Random Forest Classifier trained on the **Pima Indians Diabetes Dataset**.

---

## 🚀 Quick Start

### 1. Clone the Repo

```bash
git clone https://github.com/iam-veeramalla/first-mlops-project.git
cd first-mlops-project
```

### 2. Install UV (python package manager)

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### 2. Create Virtual Environment

```
uv venv .mlops
source .mlops/bin/activate
```

### 3. Install Dependencies

```
uv pip install -r requirements.txt
```

## Train the Model

```
python3 train.py
```

## Run the API Locally

```
uvicorn main:app --reload
```

### Sample Input for /predict

```
{
  "Pregnancies": 2,
  "Glucose": 130,
  "BloodPressure": 70,
  "BMI": 28.5,
  "Age": 45
}
```

## Dockerize the API

### Build the Docker Image

```
docker build -t diabetes-prediction-mlops-project .
```

### Run the Container

```
docker run -p 8000:8000 diabetes-prediction-mlops-project
```

## Deploy to Kubernetes with manifests

```
kubectl apply -f k8s-deploy.yml
```

## Deploy to Kubernetes with helm chart

```
helm install diabetes-prediction-mlops-project helm-chart
```

## Delete the Deployment

```
kubectl delete -f k8s-deploy.yml
```

## Delete the Helm Chart

```
helm delete diabetes-prediction-mlops-project
```

🙌 Credits

- Created by `ABHISHEK VEERAMALLA` 
- Modified by `UJWAL PACHGHARE`