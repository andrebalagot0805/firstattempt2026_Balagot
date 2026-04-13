## Balagot

#### Framework: Svelte + Vite

#### Module: Alumni Portal - Document Request & Digital Credentials

#### Installation

To replicate and run this project follow the following steps using Windows PowerShell:

```bash
# Install Node.js
winget install OpenJS.NodeJS.LTS

# Use nvm to manage Node versions (optional)
nvm install lts
nvm use lts

# Clone the repository
git clone <repo-link-here>
cd firstattempt2026_Balagot

# Install dependencies
npm install

# Run development server
npm run dev
```

The application will be available at **http://localhost:5173/**

### AI Tools:

1. ChatGPT
2. Claude (Premium)
3. GitHub Copilot (VS Code)

### Prompt:

Create a comprehensive alumni portal for Ateneo de Davao University featuring:
- Role-based authentication (Alumni & Office Staff)
- Digital academic credentials with QR code sharing
- Multi-step document request workflow
- Biometric login (FaceID/Fingerprint)
- Staff dashboard for document processing, inventory management, and payment verification
- Professional Blue Knight branding with royal blue color scheme
- Responsive mobile design
- Real-time status tracking for document requests

### Features Implemented:

✅ **Alumni Module**
- Role-based login with biometric support
- Digital Academic Passport
- Multi-step document request (TOR, Diploma, GMC, Certification, Letter)
- Rush processing option (48-hour delivery)
- QR code secure sharing
- PDF download with 30-day expiration

✅ **Staff Module**
- Verification Dashboard (alumni verification requests)
- Document Log with barcode/QR scanning
- Inventory Alerts (stock monitoring)
- Payment Verification (unique reference codes)

✅ **Design System**
- Professional sidebar navigation
- Responsive topbar with notifications
- 27 CSS variables for complete theming
- DM Serif Display & DM Sans fonts
- "Blue Knight" royal blue branding

### Screenshots

#### 🎓 Alumni Module

##### Login Screen
![Alumni Login](images/01-alumni-login.png)
*Role selection between Alumni and Office Staff with email/password authentication, biometric login, and Google Sign-In options*

##### Alumni Dashboard
![Alumni Dashboard](images/02-alumni-dashboard.png)
*Main dashboard showing welcome message, digital credential card, quick actions, and account statistics with request count, verification status, and completed documents*

##### My Profile - Academic Passport
![Academic Passport](images/03-alumni-profile.png)
*Digital Academic Passport with verified alumni status, academic information (program, graduation date), and contact details. Options to download PDF or share credential*

##### Request Documents
![Document Request](images/04-alumni-documents.png)
*Multi-step document request form showing various document types available (TOR, Diploma, Certificate of Graduation, Certificate of Enrollment, GWA Certificate, Honorable Dismissal, Document Authentication) with pricing and processing time*

##### Full Transcript Viewer
![Transcript Viewer](images/05-alumni-transcript.png)
*Modal popup showing full transcript details including total credits (120), cumulative GPA (1.45), and graduation status (Graduated with Honors)*

---

#### 🏛️ Staff Module

##### Staff Login Screen
![Staff Login](images/06-staff-login.png)
*Login screen with Office Staff selected, showing employee number field instead of student number*

##### Staff Dashboard
![Staff Dashboard](images/07-staff-dashboard.png)
*Main staff dashboard for John Administrator showing different operations (Verification, Document Log, Process Documents, Inventory Alerts, Payment Verification) with quick actions and latest notifications*

##### Staff My Profile
![Staff Profile](images/08-staff-profile.png)
*Staff member profile (John Administrator) showing academic information and access to manage biometrics or sign out*

##### Verification Dashboard
![Verification Dashboard](images/09-staff-verification.png)
*Profile verification interface showing pending verifications and verified alumni count. Table displays student ID, name, program, and verification date submitted*

##### Document Log
![Document Log](images/10-staff-document-log.png)
*Document logging system for registrar staff with barcode/QR code scanning capabilities for automatic document tracking*

##### Process Documents
![Process Documents](images/11-staff-process-documents.png)
*Active batch processing interface showing document preparation stages:
- Pending: 2 batches ready
- In Progress: 8 batches currently processing  
- Completed: 24 batches ready to deliver
- Progress bar for current batch processing (Transcript of Records)*

##### Inventory Alerts
![Inventory Alerts](images/12-staff-inventory.png)
*Stock monitoring system showing:
- Diploma Paper: Sufficient (2,450 units, reorder from 500 units)
- Binding Materials: Critical (200 units remaining, needs reorder)*

##### Payment Verification
![Payment Verification](images/13-staff-payment.png)
*Payment verification interface showing:
- Unmatched Payments table with reference codes, amounts, and verification status
- Document Log showing recent requests with status and amounts
- Support for multiple payment methods (GCash, bank transfers)*

### Project Structure

```
src/
├── App.svelte              # Main entry point
├── app.css                 # Global styles & design system
├── main.js                 # App initialization
└── lib/
    ├── LoginNew.svelte           # Authentication with role selection
    ├── DashboardNew.svelte       # Main dashboard with sidebar navigation
    ├── MyProfile.svelte          # Alumni profile & credentials
    ├── DocumentRequest.svelte    # Multi-step document request
    ├── StaffDashboard.svelte     # Staff admin panel
    └── Counter.svelte            # (Component template)
```

### Technology Stack

- **Frontend Framework:** Svelte 5.55.1
- **Build Tool:** Vite 8.0.8
- **Styling:** CSS3 with CSS Variables
- **Fonts:** Google Fonts (DM Serif Display, DM Sans)

### Color Palette

- **Royal Dark:** #0f2347
- **Royal:** #1a3a6b
- **Royal Mid:** #2e5fa3
- **Royal Light:** #e8eef8
- **Gold:** #c9a227
- **Success:** #1a7a4a
- **Warning:** #b45309
- **Danger:** #b91c1c

### Scripts

```bash
# Development
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### Browser Support

Works on all modern browsers supporting ES6+:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)

### Future Enhancements

- [ ] Backend integration (Node.js/Express)
- [ ] Database setup (MongoDB/PostgreSQL)
- [ ] Payment gateway integration (Stripe/GCash)
- [ ] Email notifications
- [ ] QR code generation library
- [ ] Barcode scanning library
- [ ] Two-factor authentication
- [ ] Document storage & archiving
