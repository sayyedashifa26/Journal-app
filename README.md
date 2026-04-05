# Journal-app
# 📓 Glitch Diaries

A private, minimal personal journal — built as a Progressive Web App (PWA) with zero backend, zero database, and zero cost to run.

---

## ✨ Features

- **OTP Authentication** — Email-based 6-digit OTP via EmailJS to protect your entries
- **Write & Edit Entries** — Title, body, category, date with character counters
- **Categories** — Life, Work, Travel, Learning, Random
- **Search** — Instant full-text search across all entries
- **Stats Dashboard** — Total entries, writing streak, word count
- **Read Mode** — Clean, distraction-free reading view
- **Offline Support** — Works without internet after first load (PWA)
- **Installable** — Add to Home Screen on Android & iPhone like a native app
- **Local Storage** — All data stays on your device, never on a server

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, Vanilla JavaScript |
| Auth | EmailJS (OTP via email) |
| Storage | Browser `localStorage` |
| Offline | Service Worker (PWA) |
| Hosting | GitHub Pages |

---

## 📁 Project Structure

```
glitch-diaries/
├── index.html       # Main app (single file — all UI + logic)
├── manifest.json    # PWA manifest (name, icons, theme)
├── sw.js            # Service worker (offline caching)
├── icon-192.png     # App icon (192×192)
├── icon-512.png     # App icon (512×512)
└── README.md
```

---

## 🚀 Setup & Deployment

### 1. Clone the repo
```bash
git clone https://github.com/Sayyedashifa26/glitch-diaries.git
cd glitch-diaries
```

### 2. Configure EmailJS
1. Sign up at [emailjs.com](https://www.emailjs.com/)
2. Create a service and an email template with `{{otp_code}}` variable
3. In `index.html`, replace:
```js
emailjs.init('YOUR_PUBLIC_KEY');
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', { otp_code: otpCode });
```

### 3. Deploy on GitHub Pages
1. Push all files to your GitHub repo
2. Go to **Settings → Pages → Branch: main → Save**
3. Your app will be live at `https://sayyedashifa26.github.io/glitch-diaries/`

---

## 📱 Install as App

**Android (Chrome)**
> Open the site → tap the three-dot menu → *Add to Home Screen*

**iPhone (Safari)**
> Open the site → tap the Share icon → *Add to Home Screen*

Once installed, the app opens full screen with no browser bar — just like a native app.

---

## 🔒 Privacy & Security

- All journal entries are stored in **your browser's localStorage only**
- No data is sent to any server
- OTP authentication prevents unauthorized access on shared devices
- Clearing browser data will erase all entries — export regularly if needed

---

---

> *"A private space for daily writing — experiences, reflections, and everything worth remembering."*
> 
