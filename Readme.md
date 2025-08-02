# 🏥 Hospital Appointment Management System (Built with Microsoft Access)

A user-friendly and lightweight appointment management system designed using Microsoft Access. This project enables hospitals, clinics, and medical centers to manage patient records, doctor schedules, appointments, and reports — all within a single Access database.

---

## 📌 Project Summary

| Feature               | Details                                              |
|----------------------|------------------------------------------------------|
| Platform             | Microsoft Access (.accdb)                            |
| Project Type         | Desktop Database Application                         |
| Users                | Receptionist, Clinic Admin                           |
| Duration to Complete | 1–3 Days                                             |
| Target Use Case      | Small to mid-sized clinics or hospitals              |

---

## 📁 Modules Overview

The project is divided into the following modules:

- 👤 Patients — Store and manage patient information  
- 👨‍⚕️ Doctors — Manage doctor details and specialties  
- 📅 Appointments — Schedule and track doctor appointments  
- 📈 Reports — Generate daily, patient, and doctor-based reports  
- 🧭 Dashboard — A navigation form to access all modules

---

## 🧱 Database Schema

### 1. Patients Table

| Field Name | Data Type  | Description              |
|------------|------------|--------------------------|
| PatientID  | AutoNumber | Primary Key              |
| Name       | Short Text | Full name of patient     |
| Age        | Number     | Age in years             |
| Gender     | Short Text | Male, Female, Other      |
| Phone      | Short Text | Contact number           |

### 2. Doctors Table

| Field Name | Data Type  | Description              |
|------------|------------|--------------------------|
| DoctorID   | AutoNumber | Primary Key              |
| Name       | Short Text | Doctor’s full name       |
| Specialty  | Short Text | Area of expertise        |

### 3. Appointments Table

| Field Name     | Data Type  | Description                            |
|----------------|------------|----------------------------------------|
| AppointmentID  | AutoNumber | Primary Key                            |
| Date           | Date/Time  | Appointment date                       |
| Time           | Short Text | Appointment time                       |
| PatientID      | Number     | Foreign Key → Patients                 |
| DoctorID       | Number     | Foreign Key → Doctors                  |
| Reason         | Long Text  | Reason for visit                       |

---

## 🛠 Features

- Add/edit patients, doctors, and appointments through user-friendly forms  
- Dropdown (combo boxes) to select doctor or patient by name  
- Automated data validation (prevent duplicate bookings for doctor and time)  
- Default date set to Today on appointment form  
- Record confirmation after save  
- Reports:
  - Daily Appointment Report
  - Doctor Schedule Report (input prompt)
  - Patient Visit History (input prompt)  
- Form-based navigation dashboard with buttons

---

## 🧑‍💻 Technologies Used

- Microsoft Access 2016 or later  
- VBA (for logic/validation)  
- Macros (for button events)  
- Queries (for data aggregation)

---

## 🧪 How to Use

1. Download or open the .accdb file in Microsoft Access  
2. Use the Dashboard form (frm_Dashboard) to navigate  
3. Add Patients and Doctors first  
4. Create appointments via Appointment Form  
5. Run reports as needed via Dashboard buttons

---

## 🚀 Deployment Notes

- To auto-load the dashboard form:  
  - File → Options → Current Database → Display Form → frm_Dashboard  
- (Optional) Split the database for multi-user environments using Access Database Splitter

---

## 📊 Sample Queries (Step 5)

- `qry_TodayAppointments` – Appointments where [Date] = Date()  
- `qry_DoctorSchedule` – Appointments filtered by Doctor (prompt input)  
- `qry_PatientHistory` – Visit history filtered by Patient (prompt input)

---

## 📄 Sample Reports (Step 6)

- `rpt_TodayAppointments`  
- `rpt_DoctorSchedule`  
- `rpt_PatientHistory`

---

## 💡 Future Improvements

- Add login authentication (Users table)  
- Add appointment status (Scheduled, Completed, Cancelled)  
- Send email/SMS reminders via Outlook integration  
- Attach medical records or prescriptions to each visit

---

## 🧑‍🎓 Developed For

Academic or professional use for learning and real-world implementation of database management systems using MS Access.

