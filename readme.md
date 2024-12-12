<h1 align="center">✨ JobSpark ✨<br> Everyone can shine</h1>

<div align='center'>

![Cloud Computing](https://img.shields.io/badge/Cloud_Computing-%237F52FF?style=for-the-badge&logo=googlecloudstorage&logoColor=white) ![Visual Studio Code](https://img.shields.io/badge/Visual_Studio_Code-2196F3.svg?style=for-the-badge&logo=accenture&logoColor=white) ![Python](https://img.shields.io/badge/python-E58800.svg?style=for-the-badge&logo=python&logoColor=white)

   <img src='https://storage.googleapis.com/jobspark_public/preview2.jpg' style='width : 50%' />
</div>

## About

JobSpark is a platform designed to empower individuals with Down syndrome by connecting them with employment opportunities. To support the scalability, security and reliability of the platform, we implement Cloud Computing on the JobSpark application. Jobspark-Model-Api-CC is an Api Service for Jobspark Machine Learning Model, using Python Fast Api.

## 🏆 Cloud Computing Members

| No  | Name                          | Bangkit ID   | Learning Path    | University                          |
| --- | ----------------------------- | ------------ | ---------------- | ----------------------------------- |
| 1   | Rangga Arsy Prawira           | C193B4KY3686 | Machine Learning | Universitas Bina Satana Informatika |
| 2   | Dhiya Bunga Syafina Ramadhani | C297B4KX1102 | Machine Learning | UPN "Veteran" Yogyakarta            |

## 🔧 Technology and Tools

1. API and Backend Technology
   - _Backend and API end points_: REST API
   - _Framework_: Fast API
   - _Programming Language_: Python
   - _Machine Learning_: Tensorflow
   - _Storage_: Google Cloud Storage
2. Dependencies
   - fastapi
   - uvicorn
   - python-multipart
   - pillow
   - numpy
   - pandas
   - tensorflow
   - scikit-learn
   - google-cloud-storage
   - pydantic
   - python-dotenv
   - google-auth
3. Machine Learning Models
   - Model Down Syndrome Face Recognition Jobspark
   - Model Recommendation System Jobspark

# Getting Started

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git (for cloning the repository)

## Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/JobSpark-Everyone-Can-Shine/Jobspark-Model-Api-CC.git jobspark-model-api
cd jobspark-model-api
```

2. Create and activate a virtual environment:

```bash
export ENV LOCAL_MODEL_PATH=model_transfer_downsyndrome.keras
export ENV MODEL_BLOB_NAME=model_transfer_downsyndrome.keras
export ENV BUCKET_NAME=jobspark
export ENV PROJECT_ID=jobspark
export ENV SERVICE_ACCOUNT_PATH=service-account.json
export ENV DATASET_PATH=dataset.csv
export ENV SISREK_MODEL_PATH=model_sisrek_jobspark.h5
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Start the development server:

```bash
# Development with auto-reload
uvicorn main:app --reload --port 8000

# Production
uvicorn main:app --host 0.0.0.0 --port 8000
```

7. Access the API:

- API endpoints: http://localhost:8000
- Interactive API docs: http://localhost:8000/docs
- Alternative API docs: http://localhost:8000/redoc

## Project Structure

```
project_root/
├── models/
│   ├── __init__.py
│   └── schemas.py
├── services/
│   ├── __init__.py
│   ├── gcs_service.py
│   ├── image_service.py
│   └── recommendation_service.py
├── utils/
│   ├── __init__.py
│   └── data_processing.py
├── .dockerignore
├── .gitignore
├── config.py
├── dataset.csv
├── Dockerfile
├── main.py
├── model_sirek_jobspark.h5
├── model_transfer_downsyndromekers
├── readme.md
├── requirements.txt
└── service-account.json
```

## Common Issues and Solutions

1. Dependencies installation fails:

```bash
# Update pip
pip install --upgrade pip

# Install system-level dependencies (Ubuntu/Debian)
sudo apt-get install python3-dev build-essential
```

2. connection issues:

- Verify environment credentials
- Ensure you have connection internet

3. Port already in use:

```bash
# Find process using the port
lsof -i :8000

# Kill the process
kill -9 <PID>
```

## Additional Resources

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [Pydantic Documentation](https://pydantic-docs.helpmanual.io/)
- [SQLAlchemy Documentation](https://docs.sqlalchemy.org/)
- [Alembic Documentation](https://alembic.sqlalchemy.org/)

## Troubleshooting Tips

1. Check logs for detailed error messages:

```bash
tail -f logs/app.log
```

2. Enable debug mode in `.env` for more detailed error responses

3. Verify Python version compatibility:

```bash
python --version
```

4. Clear cached Python files:

```bash
find . -type d -name "__pycache__" -exec rm -r {} +
```

For project-specific questions or issues, please refer to the project's issue tracker or contact the development team.
