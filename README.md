# Customer Churn Prediction MLOps Pipeline

Production-grade machine learning pipeline for predicting customer churn using historical transaction data.

## Project Overview
- Real-time customer churn prediction
- Automated model retraining pipeline
- Model performance monitoring
- API endpoint for predictions

## Architecture
```
├── data/
│   ├── raw/
│   └── processed/
├── models/
│   ├── training/
│   └── production/
├── src/
│   ├── preprocessing/
│   ├── training/
│   ├── evaluation/
│   └── api/
├── tests/
├── config/
└── notebooks/
```

## Tech Stack
- **ML Framework**: scikit-learn
- **Tracking**: MLflow
- **Data Version Control**: DVC
- **CI/CD**: GitHub Actions
- **Containerization**: Docker
- **Serving**: FastAPI
- **Monitoring**: Prometheus

## Quick Start
```bash
# Clone repository
git clone https://github.com/company/churn-prediction.git

# Set up environment
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# Run API locally
uvicorn src.api.main:app --reload
```

## Model Training
```bash
# Pull latest data
dvc pull

# Train model
python src/training/train.py

# Run tests
pytest tests/
```

## Deployment
```bash
# Build container
docker build -t churn-prediction .

# Run container
docker run -p 8000:8000 churn-prediction
```

## API Endpoints
- `POST /predict`: Get churn prediction for a customer
- `GET /health`: Service health check
- `GET /metrics`: Model performance metrics

## Monitoring
- Model metrics tracked in MLflow
- Performance monitored via Prometheus
- Automated alerts on metric degradation

## Development Process
1. Create feature branch
2. Make changes
3. Run tests
4. Create pull request
5. Automated CI checks
6. Review and merge

## Team
- ML Engineers:
- Data Scientists: 
- DevOps: 

## Links
- Documentation: 
- Model Registry: 
- Monitoring:
