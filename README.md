
# 🚀 Influencer Insights Chrome Plugin  

## 📌 Overview  
**Influencer Insights** is a Chrome plugin designed to help influencers analyze YouTube video comments efficiently. It provides sentiment analysis, comment summarization, and additional insights to improve audience engagement.  

Due to the vast volume of comments influencers receive, manual analysis is impractical. This tool leverages **NLP and Machine Learning** to extract valuable insights and trends from comments, enabling data-driven content strategy improvements.  

## 🎯 Key Features  
- **Sentiment Analysis:** Categorizes comments as **positive, neutral, or negative** with visualization.  
- **Comment Summarization:** Extracts key themes and frequent feedback.  
- **Word Cloud:** Identifies trending topics within comments.  
- **Spam & Troll Detection:** Filters out irrelevant or harmful comments.  
- **Trend Tracking:** Observes sentiment fluctuations over time.  
- **Export Analysis:** Download insights in CSV/PDF formats.  

## 🏗️ Tech Stack  
### 🔹 Backend & ML  
- **Python** (Flask, scikit-learn, spaCy, NLTK)  
- **Machine Learning** (MLflow, Optuna)  
- **Data Processing** (Pandas, NumPy)  

### 🔹 Frontend  
- **JavaScript, HTML, CSS** (Chrome Extension APIs)  

### 🔹 MLOps & Infrastructure  
- **CI/CD:** GitHub Actions  
- **Containerization:** Docker  
- **Cloud Services:** AWS (EC2, S3, CodeDeploy, IAM, CloudWatch)  
- **Data Versioning:** DVC  

## 🛠️ Project Workflow  
1. **Data Collection & Preprocessing**  
2. **Exploratory Data Analysis (EDA)**  
3. **Model Training & Experiment Tracking**  
4. **DVC Pipeline & Model Registry**  
5. **Flask API Development**  
6. **Chrome Extension Development**  
7. **CI/CD Setup**  
8. **Docker Image Creation & AWS Deployment**  

## 🔄 CI/CD Pipeline  
Our **Continuous Integration and Deployment (CI/CD)** process is managed via **GitHub Actions** and includes:  
✔️ **Code Checkout & Dependency Management**  
✔️ **Data & Model Versioning (DVC)**  
✔️ **Model Testing (Unit & Performance Tests)**  
✔️ **Automated Deployment to AWS**  
✔️ **Docker Image Build & Push to AWS ECR**  
✔️ **AWS CodeDeploy for EC2 Deployment**  

## 🚀 Deployment Steps  
This project is deployed using **AWS EC2 & AWS CodeDeploy**. To deploy manually:  
```bash
# Set up AWS credentials
aws configure set aws_access_key_id <ACCESS_KEY>
aws configure set aws_secret_access_key <SECRET_KEY>

# Push the latest Docker image to ECR
docker build -t influencer-insights .
docker tag influencer-insights:latest <AWS_ECR_REPO>:latest
docker push <AWS_ECR_REPO>:latest

# Deploy via CodeDeploy
aws deploy create-deployment \
  --application-name influencer-insights \
  --deployment-group-name influencer-insights-group \
  --s3-location bucket=<S3_BUCKET>,key=deployment.zip,bundleType=zip
```

## 📝 Running Locally  
### Prerequisites  
- Python 3.10  
- Docker  
- AWS CLI configured  

### Setup  
```bash
# Clone the repository
git clone https://github.com/your-repo/influencer-insights.git
cd influencer-insights

# Install dependencies
pip install -r requirements.txt

# Start Flask API
python flask_app/app.py
```

### Running Tests  
```bash
pytest scripts/test_load_model.py
pytest scripts/test_model_signature.py
pytest scripts/test_model_performance.py
pytest scripts/test_flask_api.py
```

## 📌 Contribution Guidelines  
- Fork the repository  
- Create a feature branch (`git checkout -b feature-name`)  
- Commit changes (`git commit -m "Add feature"`)  
- Push to branch (`git push origin feature-name`)  
- Open a **Pull Request**  

