# 🌟 Dvaltor Smart Fashion AI – Backend API 🧠👕

[![Build Status](https://img.shields.io/github/actions/workflow/status/Dvaltor-Fashion-App/Dvaltor_Backend/docker-autobuild.yml?branch=main&label=Build&style=flat-square)](https://github.com/Dvaltor-Fashion-App/Dvaltor_Backend/actions)
[![Docker Pulls](https://img.shields.io/docker/pulls/dvaltor/skin-tone-api?style=flat-square&logo=docker)](https://hub.docker.com/r/dvaltor/smart-fashion-api)
[![GitHub repo size](https://img.shields.io/github/repo-size/Dvaltor-Fashion-App/Dvaltor_Backend?style=flat-square)](https://github.com/Dvaltor-Fashion-App/Dvaltor_Backend)
[![License](https://img.shields.io/github/license/Dvaltor-Fashion-App/Dvaltor_Backend?style=flat-square)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/Dvaltor-Fashion-App/Dvaltor_Backend?style=flat-square)](https://github.com/Dvaltor-Fashion-App/Dvaltor_Backend/commits/main)

Welcome to the **backend** of 🧥 **Dvaltor's Smart Fashion AI**, a cutting-edge fashion tech platform built for intelligent clothing suggestions, personalized style, and tone-based outfit matching! 💃🕺

---

## 🚀 Live Demo

> Coming soon on:  
🌐 **https://dvaltor.com**  
🧪 API playground: `https://api.dvaltor.com/predict`

---

## 🧰 Tech Stack

**Frontend**:  
🎨 [Next.js](https://nextjs.org/) + [Tailwind CSS](https://tailwindcss.com/) + [TypeScript](https://www.typescriptlang.org/)

**Backend**:  
⚙️ [FastAPI](https://fastapi.tiangolo.com/)  
📦 Dockerized with GitHub Actions auto-build  
🌐 CORS-configured to work with multiple environments

**Database**:  
🗄️ PostgreSQL

**AI/ML Model**:  
🧠 TensorFlow model for skin tone or image classification  
📸 Accepts image uploads and returns the best match with confidence

**Deployment**:  
☁️ Docker Hub  
☁️ Google Cloud / AWS (Planned)

---

## 🔐 CORS Config (Cross-Origin Requests)

This FastAPI project is set up with:
```python
allow_origins = ["*", "https://dvaltor.com", "https://app.dvaltor.com"]
````

So it works both during development **and** production deployments.
Also supports credentials and all headers/methods! ✅

---

## 📦 API Usage

**Upload an image** to `/predict` endpoint:

### Request

```http
POST /predict
Content-Type: multipart/form-data
```

### Form Field

* `file`: 🖼️ Upload image (.jpg/.png)

### Sample Response

```json
{
  "class": "Golden Brown",
  "confidence": 0.9674
}
```

---

## 🐳 Docker Build

```bash
# Build the Docker image
docker build -t dvaltor/smart-fashion-api ./API

# Run the container
docker run -p 8000:8000 dvaltor/smart-fashion-api
```

The Docker image is **automatically rebuilt** using GitHub Actions whenever code is pushed to `main`! 🔁

---

## 📁 Project Structure

```
Dvaltor_Backend/
│
├── API/
│   ├── main.py              # FastAPI application
│   ├── Dockerfile           # Docker config
│   ├── model/
│   │   └── skin_tone_model.pkl
│   └── ...
│
├── .github/workflows/
│   └── docker-autobuild.yml # CI/CD pipeline
│
└── README.md
```

---

## 🤝 Contributing

We welcome all developers, AI enthusiasts, and fashion tech nerds to collaborate!

* Fork it 🍴
* Create your branch `git checkout -b feat/amazing-feature`
* Commit your changes 🎯
* Push to the branch `git push origin feat/amazing-feature`
* Create a PR 🚀

---

## 🧑‍💻 Maintainers

👤 [@atul-sharma](https://github.com/atulsharmaai) – Full Stack Dev & AI Engineer
🔗 [@Dvaltor-Fashion-App](https://github.com/Dvaltor-Fashion-App)

---

## 📃 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 💬 Connect with Dvaltor

Follow updates on:

* 🌐 Website: [https://dvaltor.com](https://dvaltor.com)
* 🧵 Twitter: [@dvaltor](https://twitter.com/dvaltor) *(Coming soon)*
* 🛍️ Launching soon on the Play Store & Web!

---

> ✨ **Dvaltor: Where AI meets Style** 👗👕👠
