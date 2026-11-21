Markdown
# 🎓 Student Course Registration System

<div align="center">

### ASP.NET Core MVC | C# | Razor Views

A simple web app for registering students in courses, built with **ASP.NET Core MVC** for my .NET Technologies self-learning activity.

<br>

![.NET](https://img.shields.io/badge/.NET-10.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-Programming-239120?style=for-the-badge&logo=csharp&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-MVC-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual%20Studio-IDE-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)

</div>

---

## 📌 About The Project

The **Student Course Registration System** is a web app built with ASP.NET Core MVC and C#.

It lets users register students by filling in their personal and course details. You can also view a list of all registered students and click on any student to see their full profile.

This project shows how the **Model-View-Controller (MVC)** pattern works in practice, along with Razor Views, URL routing, automatic form data binding, and input validation.

To keep things simple, the app stores student records temporarily in the computer's memory instead of using a database.

## ✨ Features

- 🏠 **Home Page** – A clean starting page with links to navigate the app.
- 📝 **Student Registration** – Add new students with their name, email, course, and semester.
- 📋 **Student List** – View all registered students in an easy-to-read table.
- 👤 **Student Details** – Check the complete profile of a single student.
- ✅ **Form Validation** – Automatically checks if the user entered valid information.
- 🔗 **MVC Routing** – Smoothly moves between different pages and actions.
- ⚡ **Model Binding** – Automatically connects form inputs to C# properties.
- 🔍 **Validation Handling** – Uses `ModelState.IsValid` to make sure data is correct before saving.

## 🛠️ Technologies Used

| Technology | What It Does |
|---|---|
| C# | Main programming language |
| ASP.NET Core MVC | Framework used to build the web app |
| .NET 10 | Underlying software platform |
| Razor Views | Creates dynamic web pages |
| HTML | Builds the structure of the web pages |
| CSS | Adds styling and layout design |
| Visual Studio | Code editor and development tool |
| Git & GitHub | Tracks code changes and hosts the project online |

## 🏗️ Project Structure

```text
self_learning/
│
├── Controllers/
│   ├── HomeController.cs
│   └── StudentController.cs
│
├── Models/
│   └── Student.cs
│
├── Views/
│   ├── Home/
│   │   ├── Index.cshtml
│   │   └── Privacy.cshtml
│   │
│   ├── Student/
│   │   ├── Create.cshtml
│   │   ├── Index.cshtml
│   │   └── Details.cshtml
│   │
│   ├── Shared/
│   │   ├── _Layout.cshtml
│   │   └── _ValidationScriptsPartial.cshtml
│   │
│   ├── _ViewImports.cshtml
│   └── _ViewStart.cshtml
│
├── wwwroot/
│
├── Properties/
│
├── appsettings.json
├── Program.cs
├── self_learning.csproj
└── README.md
📚 How MVC Works in This App
This app is organized into three main parts: Model, View, and Controller.


1. Model
The Student.cs file defines what a student looks like in the code and sets the rules for valid input.

Fields:


•	Id
•	Name
•	Email
•	Course
•	Semester
2. View
Razor Views are the web pages that users see and interact with.

View	What It Shows
Home/Index.cshtml	The main welcome page
Student/Create.cshtml	The form to register a new student
Student/Index.cshtml	The table listing all students
Student/Details.cshtml	The full details of one specific student
3. Controller
The StudentController.cs file handles user actions and decides what happens next.

Action Method	What It Does
Index()	Shows the list of all registered students
Create() GET	Opens the empty registration form
Create() POST	Checks the form data and saves the new student
Details(int id)	Finds and displays one student's details
✅ Input Validation Rules
The app uses C# Data Annotations to check user input on the server before saving it.

Rule	What It Checks
[Required]	Makes sure the field is not left blank
[StringLength]	Limits how many characters can be typed
[EmailAddress]	Checks that the text is a real email format
[Range(1, 8)]	Ensures the semester is a number between 1 and 8
ModelState.IsValid checks if all these rules pass before adding the student to the list.


🔄 How the App Flows
Plaintext
          🏠 Home Page
                |
                ▼
      Student Registration
                |
                ▼
       Enter Student Details
                |
                ▼
         Submit the Form
                |
                ▼
        Check Input Rules
                |
          ┌─────┴─────┐
          ▼           ▼
       Invalid      Valid
          |           |
          ▼           ▼
     Show Errors   Save Student
          |           |
          ▼           ▼
    Registration   Student List
        Form           |
                       ▼
                View Student Details
🚀 How to Run This Project
Follow these steps to run the app on your own computer.


What You Need First
Make sure you have installed:


•	.NET 10 SDK
•	Visual Studio (with the ASP.NET and web development workload)
•	Git
Setup Steps
Step 1: Download the project


Bash
git clone [https://github.com/meetpithadiya123/.NET_self_learning.git](https://github.com/meetpithadiya123/.NET_self_learning.git)
Step 2: Open the project folder


Bash
cd .NET_self_learning
Step 3: Find the project file

Go into the folder that contains self_learning.csproj.

Step 4: Install required packages


Bash
dotnet restore
Step 5: Start the app


Bash
dotnet run
Step 6: Open in your browser

Click or copy the https://localhost:... link shown in your terminal to view the app.

(Tip: You can also open the project in Visual Studio and press F5 to run it.)


🌐 App URLs
Page	Web Address
Home	/
Student Registration	/Student/Create
Student List	/Student/Index
Student Details	/Student/Details/1
📸 Screenshots
Here is how the app looks in action:


🏠 Home Page
📝 Student Registration Form
⚠️ Form Validation
📋 Student List
👤 Student Details
⚠️ Important Note
This app saves student records in a temporary in-memory List<Student>.


•	You do not need to set up a database.
•	Saved students stay visible as long as the app is running.
•	All records are cleared once you stop or restart the app.
This setup was chosen because a database was not required for this self-learning activity.


🎯 What I Learned
Building this project helped me understand:


•	The basics of ASP.NET Core MVC.
•	How MVC projects are structured and organized.
•	How to create Models, Controllers, and Razor Views.
•	How URL routing and controller actions work together.
•	Using Razor syntax and Tag Helpers in HTML.
•	Connecting form inputs to C# models (Model Binding).
•	Validating user input with Data Annotations and ModelState.IsValid.
•	Managing and sharing code using Git and GitHub.
🔮 Future Improvements
Here are a few ways this project can be upgraded later:


•	Connect a real database using SQL Server and Entity Framework Core.
•	Add options to edit or delete existing student records.
•	Add a search bar and filters to find students faster.
•	Add user login and role-based access (Admin/Student).
•	Upgrade the design to look even better on mobile screens.
👨‍💻 Author
Meet Pithadiya

B.Tech Computer Engineering

Marwadi University

📌 Subject: .NET Technologies (01CE1523)

📚 Semester: 5

🔗 GitHub Repository:

.NET Self Learning – Student Course Registration System


⭐ Thank You for Visiting!
Built with ❤️ using ASP.NET Core MVC and C#
