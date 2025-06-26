# ResumeScreenerApp

## Overview
This is an AI-Based Resume Screener built with ASP.NET Core and ML.NET.  
It allows you to upload resumes and score them against job descriptions using a trained ML model.
<img width="465" alt="Screenshot 2025-06-26 at 12 57 58 AM" src="https://github.com/user-attachments/assets/d5215241-85d8-43f0-9e9b-39632abb70a1" />

---

## Prerequisites

- [.NET SDK 9.0](https://dotnet.microsoft.com/en-us/download/dotnet/9.0) installed
- (Optional) [Visual Studio 2022+](https://visualstudio.microsoft.com/downloads/) or your preferred IDE
- Your trained ML model file `ResumeScorer.mlmodel` placed in `ResumeScreenerApp/MLModel/`

---

## Setup & Run

1. **Clone or download** this repository and open a terminal in the `ResumeScreenerApp` folder.

2. **Restore dependencies:**

   ```bash
   dotnet restore
Build the project:

dotnet build

Run the application:

dotnet run

Access the frontend:

Open your browser and go to http://localhost:5292/index.html

How to Use


Paste your Resume Text and Job Description into the respective text areas on the page.

Click Score Resume to send data to the backend API.

The predicted suitability score will appear below the form.

Project Structure

wwwroot/index.html — simple frontend interface to test resume scoring.

Controllers/ResumeController.cs — backend API controller exposing scoring endpoints.

MLModel/ResumeScorer.mlmodel — trained ML.NET model file.

Startup.cs — configures services and static files middleware.

Program.cs — starts the web host.

Notes

Ensure your ML model is trained and placed correctly in MLModel/.

The app serves static files from wwwroot/.
API endpoints are available under /api.
