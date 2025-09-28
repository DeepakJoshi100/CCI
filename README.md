EduManage - Institute Management System
EduManage is a modern, single-page web application built for educational institutes to manage students, batches, fees, and financial records — all in one place. Built with Firebase Firestore as the backend and vanilla JavaScript + Chart.js for the frontend, it offers real-time data sync, responsive design, and an intuitive admin dashboard.

✨ Features
📊 Dashboard
Real-time stats: Total students, batches, revenue, pending fees
Visual charts: Student distribution by batch, monthly fee collection trends
Recent activity feed showing latest student admissions
👨‍🎓 Student Management
Add, edit, archive (soft-delete) students
Search & filter by name, father’s name, course, or batch
View/edit phone number, admission date, course, batch, and monthly fee
📚 Batch Management
Create, edit, delete batches
Assign/update students to batches
View batch-wise student lists and statistics
💰 Fee Management
Auto-generate monthly fee records for active students from admission date
Record payments with method (Cash/UPI/Card/Bank) and notes
Filter by status (Paid/Unpaid/Partial), month, year
View detailed payment history per record
Financial summary cards: Total Due, Paid, Outstanding
🗃️ All Students (Archive)
Read-only view of ALL students — including archived (“deleted”) ones
Financial summary per student: Total Due, Paid, Outstanding
Option to record new payments even for archived students
Clearly marked rows and badges for archived entries
🔐 Authentication
Email/password login
Google Sign-In support
Protected routes — redirects to login if not authenticated
🎨 UI/UX Highlights
Fully responsive layout (mobile/tablet/desktop)
Sidebar navigation with collapsible menu
Toast notifications for success/error messages
Modal-driven forms for data entry
Interactive charts using Chart.js
Clean, professional color scheme with iconography (Font Awesome)
🛠️ Tech Stack
Layer	Technology
Frontend	HTML5, CSS3, Vanilla JavaScript (ES6 Modules)
Charts	Chart.js
Icons	Font Awesome 6.4
Backend	Firebase Firestore
Auth	Firebase Authentication
Hosting	Any static host (Netlify, Vercel, Firebase Hosting, etc.)
⚙️ Setup Instructions
1. Clone or Download
Bash

git clone https://github.com/yourusername/edumanage.git
cd edumanage
Or just download index.html and place it in your project root.

2. Firebase Setup
Go to Firebase Console
Create a new project (e.g., “EduManage”)
Register a web app and copy the Firebase Config object
Replace the config in index.html inside the <script type="module"> tag:
JavaScript

const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_AUTH_DOMAIN",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_STORAGE_BUCKET",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};
⚠️ Important: Enable Firestore Database and Authentication (Email/Password + Google) in Firebase Console.

3. Folder Structure
text

edumanage/
├── index.html          # Main SPA (this file)
├── login.html          # Login page (not included — create separately)
├── css/
│   ├── style.css       # Main styles
│   └── responsive.css  # Mobile adaptations
└── README.md           # This file
💡 You can keep everything in one folder — no build step required!

4. Deploy
Host index.html and /css folder on any static hosting service:

Firebase Hosting
Netlify
Vercel
GitHub Pages
Example using Firebase Hosting:

Bash

npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
🧭 Navigation
Use sidebar or URL hash to jump between sections:

#dashboard — Overview with charts
#students — Active student management
#batches — Batch creation & assignment
#fees — Payment recording & tracking
#all-students — Full archive including deleted students
📝 Notes for Developers
All data is cached per session to reduce Firestore reads.
Uses client-side routing via window.location.hash.
Global modules (App, Students, Fees, etc.) exposed to window for onclick handlers.
Includes anti-double-submit guards on forms.
Automatically generates missing monthly fee records for enrolled students.
Archived students remain in DB with deleted: true flag — never truly deleted.
🚀 Future Enhancements (Ideas)
Export reports (PDF/Excel)
Attendance tracking module
SMS/email reminders for pending fees
Role-based access (Admin, Accountant, Teacher)
Dark mode toggle
Multi-institute support
📄 License
MIT License — Free to use, modify, and distribute for personal or commercial projects.

🙋 Support
Found a bug? Have a feature request?
👉 Open an issue on GitHub or contact the developer.

✅ Built with ❤️ for educators, by developers.
Empower your institute with smart, simple management. Welcome to EduManage!
