# Inkswift Frontend (DocSign Client)

A modern, production-ready React application for document e-signature workflows, inspired by DocuSign. Built with React 18+, Tailwind CSS, React-PDF, PDF-lib, and Framer Motion.

---

## 🚀 Features
- **Secure Authentication** (JWT, protected routes)
- **PDF Upload & Preview** (drag-and-drop, URL, or file picker)
- **Signature Placement** (drag, resize, rotate, delete, multi-page)
- **Signature Creation** (draw, type, or upload image)
- **Token-based Public Signing** (secure, one-time links)
- **PDF Signature Embedding** (with PDF-lib)
- **Audit Trail** (view all signature and document actions)
- **Mobile Responsive & Accessible**
- **Modern UI/UX** (Framer Motion, custom palette, Inter font)

---

## 🖥️ Tech Stack
- **React 18+**
- **Tailwind CSS 3**
- **React Router v6**
- **Framer Motion** (animations)
- **React-PDF** (PDF viewing)
- **PDF-lib** (PDF manipulation)
- **Zustand** (state management)
- **Axios** (API calls)

---

## 📦 Project Structure
```
client/
├── public/           # Static assets
├── src/
│   ├── components/   # Reusable UI & PDF/signature components
│   ├── context/      # Auth context
│   ├── pages/        # Route pages (Dashboard, Upload, Sign, Audit, etc.)
│   ├── utils/        # Utility functions (coordinate transforms, PDF helpers)
│   └── ...
├── tailwind.config.js
├── Dockerfile
└── ...
```

---

## ⚡ Quick Start

### 1. Install dependencies
```bash
cd client
npm install
```

### 2. Environment Variables
Create a `.env` file in `client/` (optional for API proxy):
```
REACT_APP_API_URL=http://localhost:5000
```

### 3. Run the app
```bash
npm start
```
- App runs at [http://localhost:3000](http://localhost:3000)
- Backend API should be running at the URL in your `.env` or `package.json` proxy

---

## 📝 Usage Overview
- **Dashboard**: View, search, and filter your uploaded documents
- **Upload**: Drag-and-drop or select a PDF to upload and preview
- **Signature Placement**: Click to add, drag to move, resize, rotate, or delete signature fields
- **Signature Creation**: Draw (with mouse/touch), type (choose font), or upload an image
- **Public Signing**: Share secure links for others to sign without an account
- **Audit Trail**: View all actions (signed, viewed, invited, etc.) for each document

---

## 🛡️ Security & Best Practices
- All API calls use JWT for authentication
- Only PDF files are accepted for upload (validated client & server side)
- Signature data is never stored in the frontend; only sent to the backend
- Audit logs are available for every document
- Accessibility: Keyboard navigation, ARIA labels, color contrast

---

## 🐳 Docker Deployment
Build and run the production container:
```bash
docker build -t docsign-client .
docker run -p 3000:3000 docsign-client
```

---

## 🛠️ Scripts
- `npm start` – Start dev server (with HTTPS)
- `npm run build` – Build for production
- `npm test` – Run tests

---

## 🤝 Contributing
PRs and issues welcome! Please follow best practices and keep code modular and accessible.

---

## 📄 License
MIT
