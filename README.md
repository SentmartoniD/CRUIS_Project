# Student Services Portal – Azure Service Fabric, ASP.NET Core & React

A cloud-based student services web application for managing student registration, course enrollment and grades, built during my master's studies as a project for the course *Cloud Computing in Infrastructure Systems* (Serbian: *Cloud računarstvo u infrastrukturnim sistemima*, CRUIS) at the Faculty of Technical Sciences, University of Novi Sad.

## Tech Stack

- **Frontend:** React (single-page application)
- **Backend:** ASP.NET Core Web API (C#)
- **Platform:** Azure Service Fabric (microservices)

## Architecture

- **Microservices on Azure Service Fabric:** the backend is split into separate services deployed and managed on a Service Fabric cluster
- **ASP.NET Core Web API** as the entry point that communicates with the frontend and routes requests to the backend services
- **React frontend** communicating with the backend through a REST API

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
2. Open the solution in Visual Studio (as administrator).
3. Build and deploy the application to the local cluster.

### Frontend
1. Go to the frontend folder and install dependencies: `npm install`
2. Start the app: `npm start`

---

*Developed as a university project*
