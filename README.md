# 🧬 Diabetes Detection using Cutting-Edge Machine Learning

![Banner](https://raw.githubusercontent.com/aniket0657/assets/main/diabetes_banner.png)

This project leverages machine learning to predict the onset of diabetes in individuals based on medical parameters. It includes model development, evaluation, and full deployment using Docker, GitHub Actions, and AWS (EC2, ECR).

---

## 📌 Features

- Predicts likelihood of diabetes using LightGBM and Logistic Regression
- Built scalable Flask API for real-time inference
- Dockerized and deployed using GitHub Actions
- Hosted on AWS EC2 with ECR integration
- Full MLOps workflow: CI/CD + secrets management + self-hosted runners

---

## 🖼️ Demo

![App Screenshot](https://raw.githubusercontent.com/aniket0657/assets/main/diabetes_demo.png)

---

## 🧠 Algorithms Used

- Logistic Regression
- Random Forest
- LightGBM (Best model: ~86% Accuracy)

---

## 📦 Tech Stack

| Category        | Tools Used                                     |
|----------------|--------------------------------------------------|
| ML Framework   | Scikit-learn, LightGBM                          |
| Backend        | Flask                                           |
| Containerization| Docker, Docker Compose                         |
| Cloud          | AWS EC2, AWS ECR                                |
| CI/CD          | GitHub Actions, GitHub Secrets                  |

---

## 📁 Folder Structure

```
├── app/
│   ├── app.py                  # Flask application
│   └── model.pkl               # Trained ML model
├── Dockerfile
├── .github/workflows/
│   └── deploy.yml              # GitHub Actions workflow
├── requirements.txt
└── README.md
```

---

## ⚙️ How to Run Locally

### Clone the Repo
```bash
git clone https://github.com/aniket0657/diabetes-detection.git
cd diabetes-detection
```

### Build & Run with Docker
```bash
docker build -t diabetes-api .
docker run -p 5000:5000 diabetes-api
```

### Test API
```bash
curl -X POST http://localhost:5000/predict \
    -H "Content-Type: application/json" \
    -d '{"Glucose":130, "BMI":33.6, "Age":50, ...}'
```

---

## ☁️ Deployment Steps (CI/CD)

### GitHub Actions Workflow
- Push to `main` triggers Docker build
- Image pushed to AWS ECR
- EC2 instance pulls image and runs container

### Required GitHub Secrets
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `ECR_REPO`
- `AWS_DEFAULT_REGION`

---

## 📊 Dataset Used

- [Pima Indian Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)
- Features: Pregnancies, Glucose, Blood Pressure, Skin Thickness, Insulin, BMI, Diabetes Pedigree, Age

---

## 🛠️ Future Work

- Add monitoring & alerting (Prometheus/Grafana)
- Improve model explainability (SHAP, Lime)
- Automate data drift detection and retraining

---

## 🙋‍♂️ Author

**Aniket Yadav**  
[GitHub](https://github.com/aniket0657) • [LinkedIn](https://www.linkedin.com/in/aniket0657)

---

> Banner & logo assets from Freepik. README styled for clarity, visual appeal, and recruiter engagement.
