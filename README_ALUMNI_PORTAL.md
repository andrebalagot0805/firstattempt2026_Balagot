# Ateneo de Davao Alumni Portal 🛡️

A comprehensive, modern alumni portal for Ateneo de Davao University featuring digital document processing, identity verification, and administrative dashboards.

## 📋 Overview

This is a full-featured alumni management system built with **Svelte** and **Vite**, designed to serve two main user types:

- **Alumni**: Request and manage academic documents digitally
- **Office Staff**: Verify alumni, manage inventory, handle payments, and log documents

## ✨ Key Features

### 📚 Common Features (All Users)
- **Professional Login Screen** with role selection
- **Biometric Authentication** (FaceID/Fingerprint)
- **Digital Academic Passport** - Verified, shareable credentials
- **My Profile** - Personal & academic information

### 👤 Alumni Features
- **Digital Document Request Form** with multi-step wizard
  - 5 document types (TOR, Diploma, GMC, Certification, Letter)
  - Purpose-based guidance system
  - Requirements checklist
  - Real-time fee calculations
  - Rush processing option (48-hour turnaround for ₱500)
  
- **Request History** with:
  - Status tracking
  - PDF download with QR authentication
  - 30-day expiration on documents
  - Share-friendly links

### 👥 Staff Features
- **Verification Dashboard**
  - Batch year and status filters
  - Alumni verification management
  - Summary statistics
  
- **Document Logging** (Registrar)
  - Barcode/QR code scanning
  - Automatic logging (no typing needed)
  - Error reduction during busy periods
  
- **Inventory Management**
  - Stock level monitoring
  - Critical alerts for low supplies
  - Automatic reorder notifications
  - Prevents graduation delays
  
- **Payment Verification** (Finance)
  - Unique reference codes per payment
  - Prevents mix-ups with duplicate amounts
  - Status tracking
  - Alumni payment matching

## 🎨 Design & Branding

### Color Scheme (Blue Knight Theme)
- **Primary Blue**: #0052CC
- **Dark Blue**: #003BA3
- **Light Blue**: #E8F0FF
- **Success Green**: #28A745
- **Warning Orange**: #FFA500
- **Danger Red**: #DC3545

### Responsive Design
- Mobile-first approach
- Works on all screen sizes
- Touch-friendly interface

## 📁 Project Structure

```
src/
├── App.svelte              # Main app entry point with routing
├── app.css                 # Global theme and CSS variables
├── main.js                 # Svelte app initialization
├── index.html              # HTML entry point
└── lib/
    ├── Login.svelte             # Authentication & role selection
    ├── Dashboard.svelte         # Navigation & module routing
    ├── MyProfile.svelte         # User profile & digital passport
    ├── DocumentRequest.svelte   # Alumni document request system
    └── StaffDashboard.svelte    # Admin panel (verification, inventory, payments)
```

## 🚀 Getting Started

### Installation
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### First Login
- Navigate to `http://localhost:5173`
- Select role: **Alumni** or **Office Staff**
- Student Number: `20190034` (demo)
- Password: any value
- Or use **Biometric Login**

## 📋 User Stories Implemented

### Alumni Personas

| User | Pain Point | Solution | Feature |
|------|-----------|----------|---------|
| Bea Christina Cale | Uncertain about alumni legitimacy | Mandatory verification | ✓ Biometric login |
| Justin Jade Cabrera | Can't travel for document signatures | Digital-only processing | ✓ Complete request form online |
| Beatrice Joy Donton | No verified proof of degree | Auto-synced digital passport | ✓ Shareable certificate with QR |
| Maria Clara Ramos | Forgot student ID after 10 years | | ✓ Biometric login without ID |
| Princess Anaver Alcuizar | Don't know request status | Real-time tracking | ✓ Status preview & tracking |
| Keshia Angela Jardiel | Confused about document types | Purpose-based guide | ✓ "Help me choose" feature |

### Staff Personas

| User | Pain Point | Solution | Feature |
|------|-----------|----------|---------|
| Shaira Lou Manipbel | Requests across email/walk-ins | Unified dashboard | ✓ Verification dashboard |
| Jeross P. Aballe | Manual typing causes errors | Barcode scanning | ✓ Document log scanner |
| Jeross P. Aballe (2) | Stock-outs during peak weeks | Inventory alerts | ✓ Inventory management |
| Eman Torr Berjame | Have to travel for forms | Online request system | ✓ Digital form request |
| Shelley Ken Estaniel | Standard 14-day wait too long | Priority processing | ✓ Rush processing (₱500, 48h) |
| Princess Anaver Alcuizar (2) | Forget requirements | Checklist reminder | ✓ Requirements checklist |
| Bea Christina Cale (2) | PDF loss in mail | Secure digital copy | ✓ QR-authenticated PDF |

## 🔐 Security Features

- **Biometric Authentication** prevents unauthorized access
- **QR Code Verification** ensures document authenticity
- **Unique Reference Codes** track all payments
- **Session-based Routing** separates alumni/staff access
- **Encrypted Digital Documents** with expiration dates

## 🛠️ Technologies

- **Frontend**: Svelte 5.55.1
- **Build Tool**: Vite 8.0.4
- **Styling**: CSS3 with CSS Variables
- **Architecture**: Component-based, responsive design

## 📝 Document Types & Fees

| Document | Fee | Processing Time | Rush Available |
|----------|-----|-----------------|-----------------|
| Transcript of Records (TOR) | ₱150 | 3-5 days | Yes |
| Copy of Diploma | ₱200 | 5-7 days | Yes |
| Good Moral Character | ₱100 | 2-3 days | Yes |
| Course Certification | ₱175 | 3-5 days | Yes |
| Certification Letter | ₱125 | 2-3 days | Yes |

*Rush Processing: +₱500 for 48-hour turnaround*

## 🎯 Purpose Categories

1. **💼 Work/Employment** → Recommend Official Transcript or CTC
2. **🌍 Further Studies Abroad** → Recommend Official Transcript with credentials
3. **🎓 Board Exam** → Recommend Certified True Copy with seal

## 📊 Dashboard Statistics

### Alumni Dashboard
- View past requests and status
- Download documents (30-day expiration)
- Share documents via QR code
- Track payment status

### Staff Verification Dashboard
- Total requests pending/verified
- Filter by batch year
- Quick verify/reject actions
- Email notifications

### Inventory Dashboard
- Real-time stock levels
- Visual progress bars
- Alert thresholds
- One-click reorder

### Payment Dashboard
- Unique reference codes
- Status tracking (Confirmed/Pending)
- Payment matching
- Revenue tracking

## 🔄 Component Communication

- **App.svelte** manages auth state and main routing
- **Dashboard.svelte** routes between module components
- Sub-components emit events back to Dashboard for state management
- Event-based dispatch for logout functionality

## 🚧 Future Enhancements

- [ ] Backend API integration
- [ ] Database (PostgreSQL/MongoDB)
- [ ] Email notifications
- [ ] Payment gateway (PayMongo/GCash)
- [ ] Actual QR code generation
- [ ] Actual barcode scanning library
- [ ] Document upload/storage (AWS S3/Firebase)
- [ ] Admin analytics dashboard
- [ ] Multi-language support
- [ ] Two-factor authentication
- [ ] Document preview before download
- [ ] Logging and audit trails

## 📱 Responsive Breakpoints

- **Mobile**: < 600px
- **Tablet**: 600px - 768px
- **Desktop**: > 768px

All components are fully responsive with touch-friendly interfaces.

## 🎓 Learning Resources

This project demonstrates:
- ✓ Svelte component architecture
- ✓ State management with reactive variables
- ✓ Event dispatching and parent-child communication
- ✓ Responsive CSS Grid and Flexbox layouts
- ✓ CSS Variables for theming
- ✓ Form validation and multi-step workflows
- ✓ Conditional rendering with `{#if}` blocks
- ✓ List rendering with `{#each}` loops
- ✓ Two-way binding with `bind:`

## 📄 License

This project is for Ateneo de Davao University.

## 👥 Credits

**Senior UX Designer Prompt**: Designed for the needs of Ateneo de Davao alumni and staff.

---

**Built with ❤️ for Blue Knights 🛡️**
