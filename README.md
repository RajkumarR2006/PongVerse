# 🕹️ Pong Verse

![Logo](logo.png)

### 🚀 A futuristic twist on the classic Pong arcade game

Pong Verse reimagines the nostalgic Pong experience into a visually rich, web-based environment where retro meets modern design. Built with **HTML, CSS, and JavaScript**, the game offers a clean UI, dynamic animations, and both CPU and multiplayer modes.

---

## 📖 Table of Contents
1. [Overview](#-overview)
2. [Features](#-features)
3. [Project Structure](#-project-structure)
4. [Tech Stack](#-tech-stack)
5. [How to Play](#-how-to-play)
6. [Deployment (Nginx Setup)](#-deployment-nginx-setup)
7. [Future Improvements](#-future-improvements)
8. [Contributors](#-contributors)
9. [License](#-license)

---

## 🌌 Overview

**Pong Verse** is a modernized browser-based Pong game.  
It blends minimalist retro visuals with a cosmic theme using a background video, pixel fonts, and animated transitions.

This project helps beginners understand:
- Web design structure using HTML + CSS  
- Basic game logic with JavaScript  
- Hosting a project using **GitHub Pages** or **NGINX**

---

## 🎯 Features
- 🌠 Immersive background video and effects  
- 🧠 CPU and multiplayer gameplay  
- ⚡ Lightweight (pure HTML, CSS, JS)  
- 🧩 Easy to deploy and modify  
- 🎮 Responsive keyboard controls  

---

## 🗂️ Project Structure
PongVerse/
│
├── index.html # Landing page
├── i2.html # Game screen
├── gamedep.css # Stylesheet
├── icon.webp # Icon
├── logo.png # Logo
├── video.mp4 # Background video
│
├── js/ # JavaScript logic (if any)
└── deploy/
└── nginx_setup.txt # Server deployment notes


---

## 💻 Tech Stack
| Technology | Use |
|-------------|-----|
| **HTML5** | Structure and layout |
| **CSS3** | Styling and visual effects |
| **JavaScript** | Interactivity and gameplay logic |
| **GitHub Pages** | Free web hosting |
| **NGINX** | Optional deployment on servers |

---

## 🎮 How to Play
1. Open `index.html` in your browser.  
2. Choose your mode:
   - **CPU ENTITY** → Play against AI.  
   - **MULTIPLAYER** → Play with another player (same screen or online setup).  
3. Use:
   - ⬆️ **Up Arrow** → Move paddle up  
   - ⬇️ **Down Arrow** → Move paddle down  
4. Prevent the ball from passing your paddle — enjoy the game!

---

## ⚙️ Deployment (NGINX Setup)

If you want to host Pong Verse on your local or cloud server:

### Step 1: Install and Start Nginx
```bash
sudo apt update
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
sudo mkdir -p /var/www/pongverse
sudo cp -r * /var/www/pongverse/
sudo chown -R www-data:www-data /var/www/pongverse
sudo chmod -R 755 /var/www/pongverse
sudo nano /etc/nginx/sites-available/pongverse
server {
    listen 80;
    server_name pongverse.local;
    root /var/www/pongverse;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
sudo ln -s /etc/nginx/sites-available/pongverse /etc/nginx/sites-enabled/
sudo rm /etc/nginx/sites-enabled/default
sudo nginx -t
sudo systemctl restart nginx
🧭 Future Improvements

🎵 Add background music and sound effects

📱 Improve mobile responsiveness

⚡ Add WebSocket multiplayer mode

🧮 Display live score and winner message

🪪 License

MIT License © 2025 Raj Kumar R

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
