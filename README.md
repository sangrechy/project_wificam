# project_wificam



````markdown
# 📷 WiFiCam – Mobile Camera Streaming over Wi-Fi

**WiFiCam** is a simple web app that enables real-time video streaming from a mobile device to another device using WebRTC and Socket.IO. It is ideal for LAN-based peer-to-peer streaming or remote viewing via Ngrok tunneling.

🔗 GitHub Repository: [https://github.com/sangrechy/project_wificam](https://github.com/sangrechy/project_wificam)

---

## 📦 Features

- 📱 Capture and stream live video from your mobile device
- 🔁 Real-time communication using WebRTC
- 🌐 View stream remotely from another device on the same network
- 🚀 Optional: Access from anywhere using Ngrok

---

## 📋 Requirements

- ✅ [Node.js](https://nodejs.org/)
- No prior global installations required

---

````

### 🛠️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/sangrechy/project_wificam.git
cd project_wificam/app
```

### 2️⃣ Install Dependencies

```bash
npm install express socket.io
```

> `path`, `fs`, `os` are built-in Node.js modules and **do not need to be installed**

---

## 📁 Folder Structure

```txt
project_wificam/
│
├── /app
│   ├── server.js              # Express + Socket.IO signaling server
│   ├── /public
│   │   ├── mobile.html        # Camera streaming client (mobile side)
│   │   ├── viewer.html        # Viewer client (to watch the stream)
│
├── README.md
├── LICENSE
```

> ⚠️ Make sure `mobile.html` and `viewer.html` are located inside the `/public` directory.

---

## ▶️ Run the Server

```bash
node server.js
```

You’ll see something like:

```txt
Server running on http://localhost:3000
```

Open in your browser:

* On mobile device: `http://<your-local-ip>:3000/mobile.html`
* On viewer device: `http://<your-local-ip>:3000/viewer.html`

> 💡 Use your LAN IP (e.g., `192.168.x.x`) — **not `localhost`** — to connect across devices.

---

## 🌐 Access from Outside Network (via Ngrok)

Sometimes devices on different networks or mobile browsers cannot access your local IP directly. Use Ngrok to tunnel your server publicly:

```bash
ngrok http 3000
```

Ngrok will give you a public HTTPS URL like:

```
https://abcd-1234.ngrok.io
```

Use these links:

* Mobile device: `https://abcd-1234.ngrok.io/mobile.html`
* Viewer device: `https://abcd-1234.ngrok.io/viewer.html`

> ⚠️ Make sure **both devices use the Ngrok link**, not local IP, in this mode.

---

## 🔐 Security Notes

* This is a demo app intended for LAN streaming
* In production:

  * Use HTTPS + Secure WebSocket (WSS)
  * Restrict access with authentication
  * Add logging and rate-limiting as needed

---

## 📜 License

This project is licensed under the **MIT License**

---

> 🎥 Built for fast and secure peer-to-peer camera streaming over Wi-Fi.

```

---

```
