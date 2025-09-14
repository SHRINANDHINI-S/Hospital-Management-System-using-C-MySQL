# Hospital-Management-System-using-C-MySQL
Hospital Management System

A simple Hospital Management System built with C++ and MySQL.
This project demonstrates how to manage patients, doctors, and appointments using a database-backed C++ application.

✨ Features

➕ Add Patients with details (name, age, gender, disease)

➕ Add Doctors with specialization

📅 Book Appointments (linking patients & doctors)

👥 View all Patients

🩺 View all Doctors

📖 View all Appointments (with patient & doctor details)

🛠️ Tech Stack

C++ (MySQL Connector/C++)

MySQL Database

📂 Database Design
CREATE DATABASE hospital_db;
USE hospital_db;

CREATE TABLE Patients (
    patient_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10),
    disease VARCHAR(100)
);

CREATE TABLE Doctors (
    doctor_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    specialization VARCHAR(100)
);

CREATE TABLE Appointments (
    appointment_id INT AUTO_INCREMENT PRIMARY KEY,
    patient_id INT,
    doctor_id INT,
    appointment_date DATE,
    FOREIGN KEY (patient_id) REFERENCES Patients(patient_id),
    FOREIGN KEY (doctor_id) REFERENCES Doctors(doctor_id)
);
