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
![Image](https://github.com/user-attachments/assets/c785b43a-0283-4adb-be7c-7ee51a12c4a7)
![Image](https://github.com/user-attachments/assets/7c026338-3829-4f6c-aa98-02664261a910)
![Image](https://github.com/user-attachments/assets/5e0e4803-3321-4a1c-a323-b3a752ae9985)
![Image](https://github.com/user-attachments/assets/ebc9b107-f346-4cc5-b0b9-4983151c10da)
![Image](https://github.com/user-attachments/assets/fdec254b-5c50-44c9-b7bb-6f5ecb977e2a)
![Image](https://github.com/user-attachments/assets/d4c03b62-1986-4159-85f7-b6a0e350605c)
![Image](https://github.com/user-attachments/assets/c7d6ce62-9322-4361-817c-93fbec8bd7ef)
![Image](https://github.com/user-attachments/assets/d99251ab-6878-4aa7-9132-830c2cde97e8)
![Image](https://github.com/user-attachments/assets/2b54e2f5-e738-44ee-8060-d933e522664c)
![Image](https://github.com/user-attachments/assets/9c05ed6f-ad43-4495-8152-d6979aee1ad8)
![Image](https://github.com/user-attachments/assets/bba2921d-af10-439d-a05b-75c132ec7cc1)
![Image](https://github.com/user-attachments/assets/710b5dec-4bf3-4630-9215-3a6c04fb2f0c)
![Image](https://github.com/user-attachments/assets/52cb8ce8-053c-4124-805e-59b894b7920f)
![Image](https://github.com/user-attachments/assets/c7469996-dc91-467d-9234-43d69b61daee)
![Image](https://github.com/user-attachments/assets/f90cca3a-517f-425e-92c3-6438313ba177)
![Image](https://github.com/user-attachments/assets/37301718-bc4b-4d05-9d10-c52f43e93cbf)



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
