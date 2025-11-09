# System Architecture –  Telynx/Facementor

---

## 🧱 Overview
FaceMentor is designed as a modular web application with three main layers:  
1. **Frontend (Client)** – User interface and experience layer  
2. **Backend (Server)** – Business logic and API layer  
3. **Database** – Persistent storage for users, sessions, and transactions

---

## 🖥️ Frontend Architecture
- **Framework:** ReactJS with Redux for state management  
- **Routing:** React Router DOM  
- **API Calls:** Axios  
- **Authentication:** JWT tokens stored in HTTP-only cookies  
- **UI Components:** Tailwind CSS + ShadCN  

---

## ⚙️ Backend Architecture
- **Framework:** Node.js with Express  
- **Authentication:** JWT-based Auth + OAuth (Google Sign-In)  
- **API Type:** RESTful APIs  
- **Core Modules:**
  - Auth & User Management
  - Mentorship Session Management
  - Payment & Wallet
  - Notifications
  - Admin Control Panel
- **3rd-Party Integrations:**
  - Stripe – payments
  - Twilio – SMS/OTP
  - AWS S3 – file uploads

---

## 🗄️ Database Schema
**Database:** MongoDB (Mongoose ODM)

**Main Collections:**
- `users`
- `mentors`
- `sessions`
- `transactions`
- `reviews`
- `notifications`

Relationships:  
- One `mentor` can have many `sessions`  
- Each `session` links to one `mentee` and one `mentor`  
- Each `transaction` links to a `session`

---

## 🔗 Communication Flow
1. Frontend sends API requests via HTTPS  
2. Backend validates requests, processes logic, and interacts with MongoDB  
3. Responses are returned in JSON format  
4. Real-time notifications handled via WebSockets (Socket.IO)

---

## ☁️ Deployment Setup
- **Frontend:** Vercel / Netlify  
- **Backend:** AWS EC2 or Render  
- **Database:** MongoDB Atlas  
- **CI/CD:** GitHub Actions for automated deployment

---

## 💡 Technical Feasibility
This architecture supports:
- Scalable microservice-ready backend
- Low latency video sessions (via WebRTC)
- Secure authentication & payment integration
- Easy future expansion into mobile app (React Native)

 
 
