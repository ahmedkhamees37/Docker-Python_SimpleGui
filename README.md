# GUI Application in Python (Tkinter)

## 📌 Project Overview

This project is a simple GUI application built using **Python** and **Tkinter**. It allows users to enter text and display it in a message box. The application is designed to run both on a local system and inside a **Docker container** with X11 forwarding or a virtual framebuffer (Xvfb).

## 🛠️ Features

- User-friendly interface with **Tkinter**.
- Input field for text entry.
- Button to display a message box.
- Cross-platform support (Windows, Linux, macOS).
- Dockerized setup for easy deployment.

## 📂 Project Structure

```
/app
│── Dockerfile
│── gui.py  # Main Python script for the GUI application
│── README.md # Project documentation
```

## 🚀 Getting Started

### 🔹 Prerequisites

Ensure you have the following installed:

- Python 3.x
- Tkinter (comes pre-installed with Python on Windows/macOS)
- Docker (for containerized execution)

### 🔹 Run Locally

1. **Clone the repository**
   ```sh
   git clone git@github.com:ahmedkhamees37/Docker-Python_SimpleGui.git
   cd your-repo-name
   ```
2. **Run the application**
   ```sh
   python gui.py
   ```

## 🐳 Running with Docker

### 🔹 Build the Docker Image

```sh
docker build -t my-gui-app .
```

### 🔹 Run the Docker Container

#### ✅ Option 1: With X11 Forwarding (Linux/macOS GUI)

```sh
xhost +local:docker
docker run -it --rm \
    -e DISPLAY=$DISPLAY \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    my-gui-app
```

#### ✅ Option 2: Headless Mode with Xvfb (Servers)

```sh
docker run -it --rm my-gui-app
```

## 🏗️ Deploying to Docker Hub

1. **Log in to Docker Hub**
   ```sh
   docker login
   ```
2. **Tag the Image**
   ```sh
   docker tag my-gui-app your-dockerhub-username/my-gui-app:latest
   ```
3. **Push the Image**
   ```sh
   docker push your-dockerhub-username/my-gui-app:latest
   ```

## 📜 License

This project is licensed under the **MIT License**. Feel free to modify and distribute it.

## 👨‍💻 Author

**Ahmed Khamis Hassan**

- GitHub: [ahmedkhamees37](https://github.com/ahmedkhamees37)
- Docker Hub: [ahmedkhamis1](https://hub.docker.com/u/ahmedkhamis1)

---

⭐ **If you find this project useful, don't forget to give it a star!** ⭐

