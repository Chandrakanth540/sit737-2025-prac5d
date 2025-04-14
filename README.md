# 🧮 Calculator Web App (Docker + Google Cloud Deployment)

This is a lightweight calculator application containerized using Docker and deployed to Google Cloud Artifact Registry.

---

## 🚀 Project Setup

### 1. Build Docker Image

```bash
docker build -t calculator .
```

---

## ☁️ Google Cloud Setup

### 2. Login to Google Cloud Platform
- Visit: [https://console.cloud.google.com](https://console.cloud.google.com)
- Login using your **Deakin email ID**

---

### 3. Install Google Cloud SDK
- Download from: [https://cloud.google.com/sdk](https://cloud.google.com/sdk)
- Install using:
```bash
./google-cloud-sdk/install.sh
```

---

### 4. Initialize Google Cloud SDK
```bash
gcloud init
```
- Select your Deakin account
- Choose your project (e.g., `sit737-25t1-kunaparedd-13fa16e`)

---

### 5. Tag the Docker Image for Artifact Registry
```bash
docker tag calculator ___________ (e.g., 'australia-southeast2-docker.pkg.dev/sit737-25t1-kunaparedd-13fa16e/calculator/calculator:latest')
```

---

### 6. Authenticate Docker for Google Artifact Registry
```bash
gcloud auth configure-docker australia-southeast2-docker.pkg.dev
```

---

### 7. Push the Image to Google Cloud
```bash
docker push ______________(e.g., 'australia-southeast2-docker.pkg.dev/sit737-25t1-kunaparedd-13fa16e/calculator/calculator:latest')
```

---

### 8. Verify Image in Google Cloud
- Go to **Google Cloud Console**
- Navigate to: **Artifact Registry → Repositories → calculator**
- Confirm that `calculator:latest` image is present

---

## 🧪 Run the Application

### 9. Run Docker Container from Cloud Image
```bash
docker run -d -p 3000:3000 _______________(e.g., 'australia-southeast2-docker.pkg.dev/sit737-25t1-kunaparedd-13fa16e/calculator/calculator:latest')
```
- Access the app at: [http://localhost:3000](http://localhost:3000)

---

### 🔧 Stop and Remove the Container
```bash
docker ps           # List running containers
docker stop <id>    # Stop the container
docker rm <id>      # Remove the container
```

---

### 🗑️ (Optional) Remove Image from Google Cloud
- You can delete the image manually from **Google Cloud Console** or using the CLI

---

## 📄 License
This project is free to use.

---

