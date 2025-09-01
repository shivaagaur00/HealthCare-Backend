# HealthCare Backend

A Django-based backend system for healthcare management, supporting **Admins**, **Doctors**, and **Patients** with session-based authentication.

**Base URL (Local):** `http://localhost:8000`  

**Authentication:** Django built-in session-based authentication  

---

## User Types

- **ADMIN**: Full system access  
- **DOCTOR**: Manage patients and appointments  
- **PATIENT**: View own data and book appointments  

---

## Key Endpoints

### Public Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/` | System info |
| POST   | `/adminsignup` | Register admin |
| POST   | `/doctorsignup` | Register doctor (needs approval) |
| POST   | `/patientsignup` | Register patient (auto-approved) |
| POST   | `/adminlogin` | Admin login |
| POST   | `/doctorlogin` | Doctor login |
| POST   | `/patientlogin` | Patient login |
| GET    | `/logout` | Logout |
| POST   | `/contactus` | Send a message |

---

### Admin Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/admin-dashboard` | Stats dashboard |
| GET    | `/admin-view-doctor` | List doctors |
| POST   | `/admin-add-doctor` | Add doctor |
| GET    | `/admin-approve-doctor` | Pending approvals |
| GET    | `/approve-doctor/<id>` | Approve doctor |
| GET    | `/admin-view-patient` | List patients |
| POST   | `/admin-add-patient` | Add patient |
| POST   | `/discharge-patient/<id>` | Discharge patient |
| GET    | `/admin-view-appointment` | List appointments |
| POST   | `/admin-add-appointment` | Add appointment |
| GET    | `/admin-approve-appointment` | Pending appointments |

---

### Doctor Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/doctor-dashboard` | Doctor stats |
| GET    | `/doctor-view-patient` | Assigned patients |
| GET    | `/search?query=...` | Search patients |
| GET    | `/doctor-view-appointment` | Appointments |
| GET    | `/delete-appointment/<id>` | Delete appointment |

---

### Patient Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET    | `/patient-dashboard` | Patient info |
| GET    | `/patient-view-doctor` | List doctors |
| GET    | `/searchdoctor?query=...` | Search doctors |
| POST   | `/patient-book-appointment` | Book appointment |
| GET    | `/patient-view-appointment` | My appointments |
| GET    | `/patient-discharge` | Discharge details |

---

## Project Setup Instructions

1. **Clone the repository**

```bash
git clone https://github.com/shivaagaur00/HealthCare-Backend.git
cd HealthCare-Backend