# 🚗 BPark — Smart Parking Management System

> A full-stack client-server platform that takes parking lot management from "circle the block and hope" to real-time, automated, and actually pleasant.
---

## 📖 What is BPark?

BPark digitizes the entire lifecycle of a parking lot — from the moment a driver reserves a spot to the automated nudge they get if they forget to pick up their car. It's built as a real client-server system: a JavaFX desktop app talks to a custom multithreaded server in real time, backed by a MySQL database.

Three roles, three experiences:

| 👤 Role | What they can do |
|---|---|
| 🧑‍💼 **Subscriber** | Reserve a spot, park, extend a session, view history, retrieve a lost code |
| 🧍 **Usher** | Manage drop-off/pick-up on-site, verify subscribers, handle walk-ins |
| 👔 **Parking Lot Manager** | Full oversight — live spot status, analytics, and reports |

---

## ✨ Key Features

- 🅿️ **Real-time spot tracking** — every space is `AVAILABLE`, `RESERVED`, or `OCCUPIED`, always up to date
- 📅 **Smart reservations** — book ahead, get a confirmation code, track status end-to-end
- ⏱️ **Live sessions** — drop-off, pick-up, and on-the-fly time extensions
- 📧 **Automated alerts** — email (and SMS) notifications when a pickup runs late
- ⏰ **Background automation** — scheduled jobs quietly keep spot statuses and late-session checks running, no human needed
- 📊 **Manager analytics** — peak usage times, spot utilization, top users, and late-parking reports, visualized as graphs
- 🙋 **Self-service** — subscribers manage their own contact info and history without calling anyone

---

## 🏗️ How it's built

```
📡 JavaFX Client  ⇄  🖧 Multithreaded Server (OCSF)  ⇄  🗄️ MySQL Database
```

- **Client** — JavaFX desktop app with dedicated screens per role
- **Server** — Custom socket server on the [OCSF] framework, routing typed requests
- **Database** — MySQL, accessed through a pooled connection layer
- **Scheduler** — Background `TimerTask` jobs for daily refreshes and late-session sweeps

## 🛠️ Tech Stack

`Java 21` · `JavaFX 21` · `MySQL` · `OCSF` · `Jakarta Mail` · `Maven` · `JUnit 5`

---

## 📂 Repository Structure

```
BparkProject/
├── 🅿️ BPark-Project/     → the actual application (source code, ready to run)
├── 📘 Assignment1/       → Assignment 1 deliverables
├── 📗 Assignment2/       → Assignment 2 deliverables (incl. prototype builds)
└── 📄 README.md         
