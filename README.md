# 🔰 Abhaya – Smart Women Safety & Emergency Alert System

> A software-based emergency alert prototype that lets a user trigger an instant distress signal, share their live location, and notify trusted contacts — all with a single tap.

---

## 🚧 Status

Early-stage prototype — frontend in progress, backend/alerts coming next. This README reflects the planned scope and will be updated as features are built.

---

## 📖 About the Project

Abhaya (अभय — "fearless / without fear") is a web/mobile application designed to give users a fast, low-friction way to send out an emergency alert when they feel unsafe. With one tap, the app captures the user's live location, generates a shareable map link, and sends an alert to pre-saved emergency contacts.

This repo currently contains a **software-only prototype** — there is no hardware, IoT, or embedded component. The focus right now is on proving the core flow (panic trigger → location capture → alert dispatch → logging) using web technologies, with hardware/IoT integration planned as a future phase.

---

## 🎯 Problem It Solves

Personal safety apps that exist today often fail at the exact moment they're needed most, because they:

- Require multiple taps, unlocking the phone, or navigating through menus during a high-stress situation
- Don't clearly communicate **where** the person is to the people who can help
- Depend on the victim staying calm and tech-literate under panic — which is unrealistic
- Are often bloated with features unrelated to the actual emergency

**Abhaya's goal** is to strip this down to the essentials: one button, instant location sharing, and automatic notification — designed so it works *especially* when the user is panicked, distracted, or has limited time to act.

---

## ✅ Current Scope (Software Prototype)

- Web/mobile application interface
- Digital panic button
- Live location sharing via browser Geolocation API
- Emergency contact management
- Alert generation and dispatch (email/SMS, simulated for prototype)
- Google Maps location link generation
- Alert history dashboard

## ❌ Out of Scope (For Now)

These are intentionally **not** part of this version — they're future-phase ideas, not missing features:

- Arduino / ESP32 or any microcontroller
- Dedicated GPS hardware modules
- GSM modules
- Any physical wearable or circuit-based device

---

## 🚀 Planned Features

### 1. 🟥 Emergency Panic Button
- One-tap emergency trigger, prominently placed in the UI
- Optional long-press trigger for accidental-press protection

### 2. 🟧 Live Location Tracking
- Uses the browser's Geolocation API to get real-time latitude/longitude
- Automatically generates a shareable Google Maps link

### 3. 🟨 Emergency Alert System
- Sends a pre-formatted alert to saved contacts:
  > "Emergency! I need help. My location: `<Google Maps link>`"
- Delivery via Email API and/or SMS API (Twilio), with simulated alerts for early-stage testing

### 4. 🟩 Contact Management System
- Add, edit, and delete emergency contacts
- Contacts stored locally or in a database depending on build stage

### 5. 🟦 Alert History Dashboard
- View past triggers, locations, and alert logs
- Simple, scannable UI for reviewing activity

### 6. 🟪 Stealth Mode UI
- Minimal, unobtrusive interface during normal use
- Panic button stays accessible without drawing attention
- Designed for low-click, fast activation

---

## 🧠 How It Works (Workflow)

```
User opens the app
        ↓
Taps the Panic Button
        ↓
Browser requests location permission
        ↓
GPS coordinates captured
        ↓
Google Maps link generated
        ↓
Alert sent to emergency contacts (email/SMS/simulated)
        ↓
Event logged in the dashboard
        ↓
Confirmation shown to user
```

---

## 💻 Tech Stack

**Frontend**
- HTML, CSS, JavaScript (or React.js)

**Backend** *(optional, recommended)*
- Node.js / Express or Python (Flask)

**APIs**
- Browser Geolocation API
- Email API (e.g., Nodemailer/SMTP)
- SMS API (Twilio — optional)

**Database**
- Firebase / MongoDB / LocalStorage (for early prototype)

---

## 📁 Project Structure

```
Abhaya-Women-Safety-System/
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── app.js
│
├── backend/
│   ├── server.js (or app.py)
│   └── alertService.js
│
├── components/
│   ├── panicButton.js
│   ├── locationService.js
│   └── contactManager.js
│
├── database/
│   ├── contacts.json
│   └── logs.json
│
├── docs/
│   ├── project_report.pdf
│   └── system_flow.png
│
└── README.md
```

---

## 🛠️ Getting Started

> This section will fill out as the project develops. For now, here's the intended setup flow:

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/Abhaya-Women-Safety-System.git
   cd Abhaya-Women-Safety-System
   ```

2. Set up the frontend
   ```bash
   cd frontend
   # open index.html in your browser, or set up a dev server
   ```

3. (Optional) Set up the backend
   ```bash
   cd backend
   npm install        # or pip install -r requirements.txt for Flask
   npm start          # or python app.py
   ```

4. Add environment variables for any APIs in use (Email/SMS), e.g. in a `.env` file:
   ```
   EMAIL_USER=your_email
   EMAIL_PASS=your_password
   TWILIO_SID=your_sid
   TWILIO_AUTH_TOKEN=your_token
   ```

---

## 🔮 Future Scope

- Native mobile app version
- Wearable / IoT device integration
- AI-based threat detection
- Background voice activation (e.g., "Help me")

---

## ⚠️ Disclaimer

This project is a prototype built for learning and demonstration purposes. It is **not** intended as a production-ready safety solution and should not be relied upon as a sole safety measure in real emergencies.
