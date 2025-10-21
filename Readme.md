# CI/CD Demo Project

This repository demonstrates a **basic CI/CD pipeline** using **GitHub Actions**. It automatically runs tests on push and deploys the application to a test environment if all tests pass. 

---

## 🗂 Project Structure
```text
ci-cd-demo/
├── app/
│ ├── init.py
│ └── main.py # Main application code
├── tests/
│ ├── init.py
│ └── test_main.py # Unit tests for the app
├── requirements.txt # Python dependencies
└── .github/
└── workflows/
├── ci.yml # Runs tests on push/PR
└── deploy.yml # Deploys app on successful tests

yaml
```
---

## ⚙️ Features

- **Continuous Integration (CI)**
  - Runs `pytest` automatically on every push or pull request.
  - Checks that your code works and passes all tests.

- **Continuous Deployment (CD)**
  - Deploys the application to a test environment if tests pass.
  - Demonstrates deployment automation using GitHub Actions.

---

## 📝 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/Samar-feki-75/ci-cd-demo.git
cd ci-cd-demo
```
### 2. Create a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # Linux / macOS
venv\Scripts\activate     # Windows

```
### 3. Install dependencies
```bash
pip install -r requirements.txt
```
### 4. Run tests locally
```bash
pytest
```
### 5. How CI/CD works
Any push to main triggers CI tests (ci.yml).

If tests pass, deployment (deploy.yml) is triggered.

Deployment currently copies app files to a temporary folder /tmp/test-deploy (can be replaced with your real environment).

## 📦 Python Dependencies
pytest - testing framework

## 🚀 How to Customize
Update deploy.yml to deploy to a real server, GitHub Pages, or cloud service.

Add more tests in tests/ for your application.

Extend the workflow with linting, coverage, or notifications.

