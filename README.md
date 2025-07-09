# project_wificam

---

````markdown
# 📷 Mobile Camera Streaming

Mobile Camera Streaming is a lightweight web app that allows real-time video streaming from a mobile device to a viewer using WebRTC and Socket.IO. It works over local network or publicly using Ngrok tunneling.

🔗 GitHub Repository: [https://github.com/sangrechy/project_wificam](https://github.com/sangrechy/project_wificam)

---

## 📂 Directory Structure

```txt
/project_wificam
│── /public
│   ├── mobile.html         # Page to capture mobile camera input
│   ├── viewer.html         # Page to view the stream
│
│── server.js               # Express server with Socket.IO for signaling
│── README.md
````

---

## 🚀 Features

* 📱 Live camera streaming from mobile device
* 🔁 Peer-to-peer connection using WebRTC
* 🔄 Real-time offer/answer and ICE exchange with Socket.IO
* 🌐 Ngrok support for remote/public access

---

## 📋 Requirements

* [Node.js](https://nodejs.org/)
* Express.js
* Socket.IO
* Ngrok (for external device access)

---

## 🛠️ Setup & Installation

### 📦 Clone the Repository

```bash
git clone https://github.com/sangrechy/project_wificam.git
cd project_wificam/app
```

### 📦 Install Dependencies

```bash
npm install express socket.io
```

### ▶️ Start the Server

```bash
node server.js
```

Now the server will run on:

```
http://localhost:3000
```

Open in browsers:

* On mobile device: `http://<your-ip>:3000/mobile.html`
* On viewer device: `http://<your-ip>:3000/viewer.html`

---

## 🌐 Ngrok for Public Access (Optional)

If your devices are not on the same network or local IP doesn’t work, use Ngrok:

```bash
ngrok http 3000
```

Ngrok will return a public URL like:

```
https://abcd-1234.ngrok.io
```

Use:

* Mobile: `https://abcd-1234.ngrok.io/mobile.html`
* Viewer: `https://abcd-1234.ngrok.io/viewer.html`

> ⚠️ Both devices must use the Ngrok link to work correctly.

---

## 🔐 Notes

* Enable camera access in browser
* Works best on the same Wi-Fi or through Ngrok
* For real deployments, use HTTPS and secure signaling

---

## 📜 License

This project is licensed under the **MIT License**.

---

> 🚀 Built for seamless peer-to-peer camera sharing across devices!

```

---

You can now copy this entire block into your GitHub repository’s `README.md`. Let me know if you also want a preview HTML version or Markdown badges.
```
