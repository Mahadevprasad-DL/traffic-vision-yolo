# Traffic Analysis System

An AI-powered Traffic Analysis System that uses **YOLOv3** for vehicle detection and **Flask** for backend processing. The application provides traffic analytics, heatmaps, and prediction dashboards, and can be containerized with Docker and deployed to Kubernetes with CI/CD automation.

---

## Features

- 🚗 Real-time vehicle detection using YOLOv3
- 📊 Traffic analytics dashboard
- 🔥 Heatmap visualization
- 📈 Traffic prediction module
- 🌐 Web interface using Flask templates
- 🐳 Dockerized application
- ☸️ Kubernetes deployment
- 🔁 CI/CD pipeline using GitHub Actions

---

## Tech Stack

- Backend: Flask (Python)
- AI Model: YOLOv3
- Computer Vision: OpenCV
- Frontend: HTML, CSS, JavaScript
- Containerization: Docker
- Orchestration: Kubernetes
- CI/CD: GitHub Actions

---

## Project Structure

```
TRAFFIC/
├── app.py
├── requirements.txt
├── Dockerfile
├── .dockerignore
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
├── .github/
│   └── workflows/
│       └── ci-cd.yaml
├── static/
├── templates/
├── yolov3.cfg
├── yolov3.weights
```

---

## Prerequisites

- Python 3.8+ (3.11 recommended)
- pip
- Docker (for container builds)
- kubectl (for Kubernetes deployments)

---

## Installation (Local Setup)

### 1. Clone Repository

```bash
git clone https://github.com/Mahadevprasad-DL/traffic-analysis-system.git
cd traffic-analysis-system
```

### 2. Create Virtual Environment

Windows:

```powershell
python -m venv venv
venv\Scripts\activate
```

Linux / macOS:

```bash
python -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Application

```bash
python app.py
```

The app will typically be available at `http://127.0.0.1:5000` unless configured otherwise.

---

## Docker Setup

### Build Docker Image

```bash
docker build -t traffic-analysis .
```

### Run Container

```bash
docker run -p 5000:5000 traffic-analysis
```

You can then open `http://localhost:5000` in your browser.

---

## Kubernetes Deployment

Apply Deployment & Service manifests:

```bash
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

Verify:

```bash
kubectl get pods
kubectl get services
```

If `service.yaml` exposes a `NodePort`, access via:

```
http://<NODE_IP>:<NODE_PORT>
```

---

## CI/CD (GitHub Actions)

A sample pipeline is included at [/.github/workflows/ci-cd.yaml](.github/workflows/ci-cd.yaml). Adjust the workflow to your cloud provider, container registry, and deployment strategy.

---

## Files of Interest

- Application entry: [app.py](app.py)
- Requirements: [requirements.txt](requirements.txt)
- YOLO config: [yolov3.cfg](yolov3.cfg)
- YOLO weights: [yolov3.weights](yolov3.weights)
- Dockerfile: [Dockerfile](Dockerfile)
- Kubernetes manifests: [k8s/deployment.yaml](k8s/deployment.yaml), [k8s/service.yaml](k8s/service.yaml)
- Templates: [templates/](templates/)
- Static assets: [static/](static/)

---

## Notes & Tips

- YOLOv3 weights are large; ensure you have [yolov3.weights](yolov3.weights) in the project root or update paths as needed.
- For production use, consider converting models to an optimized runtime (TensorRT, ONNX + ONNX Runtime) or using a smaller model (e.g., YOLOv5/YOLOv8) for improved latency.
- Secure endpoints and secrets before deploying to cloud environments (use Kubernetes Secrets or a secrets manager).

---

## Acknowledgements

- YOLOv3
- OpenCV Community
- Flask Framework
- Kubernetes & Docker Community

---

## License

This project does not include a license file by default. Add an appropriate `LICENSE` if you intend to open source this repository.

---

## 📧 Contact

For queries or collaboration, please open an issue or contact the repository owners:

- **[Manasa S](https://github.com/manasa-s7)**  
- **[Mahadevprasad-DL](https://github.com/Mahadevprasad-DL)**  
 


