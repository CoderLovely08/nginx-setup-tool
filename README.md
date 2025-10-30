# 🧩 Nginx Domain Setup Generator

A clean and intuitive **web-based tool** that generates all the necessary commands and configuration files to set up **Nginx as a reverse proxy** for **any backend application** — including optional SSL setup using **Certbot**.

---

## 🌐 Live Demo

👉 [**nginx-setup-tool.vercel.app**](https://nginx-setup-tool.vercel.app/)

---

## 🚀 Features

* 🧠 **Automatic Nginx command generator** — no need to remember syntax
* ⚙️ **Step-by-step guide** — covers installation, configuration, and SSL setup
* 🔒 **Free SSL with Certbot** — generate ready-to-run commands
* 📋 **One-click copy** — easily copy any command block
* 💻 **Works for any backend** — Node.js, Flask, FastAPI, Django, Go, PHP, etc.
* 🧾 **Responsive & beginner-friendly UI**

---

## 🧱 How It Works

1. Enter your **domain or subdomain** (e.g. `api.example.com`)
2. Enter your **application port** (e.g. `4000`)
3. Click **“Generate & Update Commands”**
4. Copy and execute the commands on your Linux server

You’ll get:

* ✅ Nginx installation commands
* ✅ Configuration setup instructions with a generated config file
* ✅ SSL setup commands (Certbot)

---

## 📖 Documentation

Detailed setup instructions:
👉 [Nginx Server Setup Guide](https://github.com/CoderLovely08/Backend-Starter/blob/main/docs/04%20Nginx%20Server%20Setup.md)

---

## 🧰 Tech Stack

* **HTML5**
* **CSS3**
* **Vanilla JavaScript**

No dependencies or frameworks — just open and use it.

---

## 🛠️ Run Locally

```bash
# Clone the repository
git clone https://github.com/your-username/nginx-setup-generator.git

# Go to the folder
cd nginx-setup-generator

# Open in browser
open index.html
```

---

## 🪄 Example Output

Example Nginx config for a backend running on port 4000:

```nginx
server {
    listen 80;
    server_name api.example.com;

    location / {
        proxy_pass http://localhost:4000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}
```

---

## ✨ Credits

Developed with ❤️ by [Lovely Sharma](https://lovelycodes.vercel.app/)

---

## 📜 License

Licensed under the **MIT License** — free to use, modify, and share.
