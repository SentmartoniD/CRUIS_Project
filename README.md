# Student Services Portal – Azure Service Fabric, ASP.NET Core & React

A cloud-based student services web application for managing student registration, course enrollment and grades, built during my master's studies as a project for the course *Cloud Computing in Infrastructure Systems* (Serbian: *Cloud računarstvo u infrastrukturnim sistemima*, CRUIS) at the Faculty of Technical Sciences, University of Novi Sad.

## Tech Stack

- **Frontend:** React (single-page application)
- **Backend:** ASP.NET Core Web API (C#)
- **Platform:** Azure Service Fabric (microservices)

## Architecture

![Architecture diagram](Dijagram.png)

The backend is built as a set of microservices running on **Azure Service Fabric**:

- **Web API** – the single entry point for the React clients, routing requests to the backend services
- **Validation Service** – validates incoming requests before they reach the business logic
- **Authentication Service** – handles user authentication and access control
- **Transaction Coordinator Service** – coordinates operations that span multiple services, keeping data consistent across them
- **Student Service** – manages student data and course enrollments
- **Professor Service** – manages professors and grade entry
- **Subject Service** – manages available courses
- **Database** – shared data storage used by the domain services

## Features

### Student
- Registers by entering personal details (first name, last name, student ID number, email)
- Views and updates personal information
- Browses available courses, enrolls in courses and withdraws from them

### Professor
- Enters grades for each student per course

### Reports
- Generates reports on average grade, academic performance and the list of enrolled courses

## Running the Project

### Backend
1. Install the Azure Service Fabric SDK and start a local Service Fabric cluster.
2. Open the solution in `back-end/StudentServiceApplication` in Visual Studio (as administrator).
3. Build and deploy the application to the local cluster.

### Frontend
1. Go to the frontend folder: `cd front-end/studentservicereactapplication`
2. Install dependencies: `npm install`
3. Start the app: `npm start`

## Project Specification

The original project specification (in Serbian) is available in [Cloud - predmetni projekat- 2024.pdf](Cloud%20-%20predmetni%20projekat-%202024.pdf).

---

*Developed as a university project. Some code comments may be in Serbian.*
