# 📷 WiFiCam — Mobile Camera Streaming over Wi-Fi

WiFiCam is a simple web application that streams live video from a mobile device to another device using **WebRTC** and **Socket.IO**.

It can be used for camera streaming over a local Wi-Fi network or through an optional Ngrok tunnel.

## ✨ Features

* 📱 Live camera streaming from a mobile device
* 🔁 Real-time WebRTC communication
* 🌐 View the camera from another device
* 🚀 Optional remote access using Ngrok

## 🛠️ Requirements

* [Node.js](https://nodejs.org/)
* A mobile device with a camera
* Devices connected to the same Wi-Fi network

## 📥 Installation

### 1. Clone the repository

```bash
git clone https://github.com/sangrechy/project_wificam.git
cd project_wificam/app
```

### 2. Install dependencies

```bash
npm install
```

If dependencies are not already listed in `package.json`:

```bash
npm install express socket.io
```

> `path`, `fs`, and `os` are built-in Node.js modules.

## 📁 Project Structure

```text
project_wificam/
├── app/
│   ├── server.js
│   └── public/
│       ├── mobile.html
│       └── viewer.html
├── README.md
└── LICENSE
```

Make sure `mobile.html` and `viewer.html` are inside the `public` folder.

## ▶️ Start the Server

Run:

```bash
node server.js
```

You should see:

```text
Server running on http://localhost:3000
```

Find the local IP address of the computer running the server.

Then open:

**Mobile:**

```text
http://<your-local-ip>:3000/mobile.html
```

**Viewer:**

```text
http://<your-local-ip>:3000/viewer.html
```

Example:

```text
http://192.168.1.5:3000/mobile.html
http://192.168.1.5:3000/viewer.html
```

> Use the computer's LAN IP instead of `localhost` when connecting from another device.

## 🌐 Remote Access with Ngrok

To access the application from outside the local network:

```bash
ngrok http 3000
```

Ngrok will provide a public HTTPS address.

Use:

```text
https://your-ngrok-url/mobile.html
```

on the mobile device and:

```text
https://your-ngrok-url/viewer.html
```

on the viewer device.

Both devices should use the same Ngrok URL.

## 🔐 Security

This project is intended mainly for testing and LAN streaming.

For production use, consider adding:

* HTTPS/WSS
* User authentication
* Access control
* Rate limiting
* Proper logging

## 📜 License

This project is licensed under the **MIT License**.

## 🔗 Repository

https://github.com/sangrechy/project_wificam
