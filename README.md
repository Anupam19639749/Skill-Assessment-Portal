# Skill Assessment Portal - Full-Stack Evaluation Platform

A comprehensive, full-stack web application designed to modernize and streamline technical skill evaluation. It provides a robust platform for administering, taking, and reviewing skill-based assessments, offering clear and actionable insights into individual proficiencies.

The application features a role-based ecosystem (**Admin**, **Evaluator**, **Candidate**) that ensures secure access and distinct workflows, fostering an efficient and transparent assessment process from creation to feedback.

---

## Key Features

### 1. Robust Assessment Lifecycle Management
* **Dynamic Assessment Creation:** Admins can easily create multi-question assessments with various question types (MCQ, True/False, Short Answer).
* **Question Bank:** Centralized management system to associate specific questions with relevant assessments.
* **Assignment & Scheduling:** Streamlined process for assigning assessments to candidates with controlled access parameters.

### 2. Secure & Streamlined User Experience
* **Role-Based Access Control (RBAC):** Distinct dashboards and functionality sets for Admin, Evaluator, and Candidate roles.
* **Secure Authentication:** Robust JWT-based login system ensures secure access and session management.
* **Inactivity Session Timeout:** Client-side security mechanism with warnings to prevent unauthorized access during idle periods.

### 3. Comprehensive Evaluation & Feedback
* **Candidate Submissions:** Candidates can access and submit their responses securely within the assigned timeframe.
* **Evaluator Dashboard:** Dedicated interface for Evaluators to review submissions, assign scores manually, and provide detailed textual feedback.
* **Results & History:** Candidates can view their complete history, including scores, pass/fail status, and specific feedback from evaluators.

### 4. Data-Driven Insights
* **Clear Performance Metrics:** Instant view of total marks obtained and percentage scores for each assessment.
* **Feedback Integration:** A Direct feedback loop visible to candidates to foster continuous improvement.

---

## 🛠️ Tech Stack

### **Backend**
* **Framework:** ASP.NET Core Web API (.NET 8)
* **Architecture:** Layered (Controllers, Services, Repositories)
* **Database:** SQL Server with Entity Framework Core
* **Authentication:** JWT (JSON Web Tokens)
* **Security:** HMACSHA512 Hashing
* **Data Mapping:** AutoMapper
* **Documentation:** Swagger/OpenAPI

### **Frontend**
* **Framework:** Angular 17
* **Language:** TypeScript
* **State Management:** Component/Service-based architecture
* **HTTP Client:** HttpClient (with Interceptors for Auth)
* **Routing:** Angular Router (with AuthGuard & RoleGuard)
* **Styling:** CSS3, Material Icons

---

## ⚙️ Setup & Installation

### Prerequisites
* Node.js & npm (LTS)
* Angular CLI (`npm install -g @angular/cli`)
* .NET 8 SDK
* SQL Server
* Git

### 1. Backend Setup
1.  Clone the repository:
    ```bash
    git clone [https://github.com/](https://github.com/)[Your GitHub Username]/Skill-Assessment-Portal.git
    ```
2.  Navigate to the backend directory:
    ```bash
    cd Skill-Assessment-Portal/skill_assessment_portal_backend
    ```
3.  **Configure Database:** Open `appsettings.Development.json` and update the Connection String to point to your SQL Server.
4.  Apply migrations to create the database schema and seed initial roles:
    ```bash
    dotnet ef database update
    ```
5.  Start the API:
    ```bash
    dotnet run
    ```
    *(The API will run on `https://localhost:7001` by default)*

### 2. Frontend Setup
1.  Navigate to the frontend directory:
    ```bash
    cd ../skill_assessment_portal_frontend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Start the Angular app:
    ```bash
    ng serve -o
    ```
    *(The app will run on `http://localhost:4200` by default)*

---

## 📖 Usage Guide

1.  **Access:** Ensure both Backend and Frontend are running. Open `http://localhost:4200`.
2.  **Admin Login:** Log in using `admin@skillportal.com` (Password: `Admin@123`).
    * *Action:* Create assessments, add questions, and assign them to candidates.
3.  **Register Candidate:** Log out and register a new user account (default role is Candidate).
4.  **Take Assessment:** Log in as the new candidate. Navigate to "My Assessments" and complete any assigned tests.
5.  **Evaluate:** Log back in as **Admin** (or an Evaluator). Go to the submissions review page, grade the answers, and leave feedback.
6.  **View Results:** As a candidate, check your "Results" page to see your score and evaluator feedback.

---

## 👤 Author

**Anupam Agrawal**
* **Role:** Full-Stack Developer
* **Project Type:** Module Assessment Project
