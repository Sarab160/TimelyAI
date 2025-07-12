# 📅 TimelyAI - Smart Timetable Generator

**TimelyAI** is an intelligent, GUI-based timetable generator built using Python and CustomTkinter. It allows users to generate and export optimized weekly timetables for multiple classes, considering teacher availability, subject types (lecture/lab), room constraints, and customizable configurations like lecture duration, break period, and time slots.

---

## 🚀 Key Features

- ✅ **Multi-Class Scheduling**: Generate full weekly timetables for one or more classes
- 🧑‍🏫 **Manual Teacher Assignment**: Users assign teachers to each subject manually
- ✅ **Smart Subject Matching**: Only valid teachers (from `teachers.json`) who teach a subject are shown
- 🕒 **Custom Start Time & Duration**: Users input the lecture start time and duration (e.g., 08:00 AM, 45 minutes)
- 🍽️ **Break Period Selection**: Select which period should be the break (e.g., Period 3)
- 🧠 **Intelligent Slot Assignment**:
  - Labs are scheduled in 3 consecutive periods
  - Retry logic ensures subjects aren't skipped easily
- 📄 **PDF Export**: Generate a clean and printable timetable PDF
- 🔍 **Entity Info Viewer**: View full teacher, class, subject, and room details
- 🔁 Auto-assigns based on constraints: availability, subjects, room, and time
- 🖥️ **CustomTkinter GUI**: Beautiful, scrollable, and responsive interface

---

## 📂 Project Structure

TimelyAI/
├── main.py # Main GUI application
├── teachers.json # Teacher details with subjects and preferences
├── subject.json # Subjects with type, duration, and lectures
├── rooms.json # List of lab and normal rooms
├── classes.json # Class names and subject mapping
├── README.md # Project documentation

## 🛠️ Technologies Used

- **Python 3**
- **CustomTkinter** - Modern and responsive tkinter GUI framework
- **FPDF** - For PDF generation
- **JSON** - Structured data format for managing entities
  
## 📋 How It Works
Load Data: Loads JSON data for teachers, rooms, classes, and subjects.

Setup: User selects:

Class(es) to schedule (e.g., A, B, C)

Start time (e.g., 08:00)

Lecture duration (e.g., 45 minutes)

Break period (e.g., Period 3)

Manual Mapping: Users assign teachers to subjects using dropdowns. Only valid teachers are shown.

Generate Timetable:

Algorithm scans available slots for all lectures and labs

Ensures rooms, teachers, and periods are not double-booked

Lab lectures are assigned in 3 continuous slots

Skipped assignments are shown in the results

Output Display: The timetable is shown for each class in a readable format.

PDF Export: A professional-looking timetable is generated as a downloadable PDF

## 📸 GUI Highlights
🎛️ Setup Page: Input classes, start time, break period, and lecture duration

🔀 Teacher Assignment Dropdowns: Select teachers manually for each subject

📑 Timetable Viewer: View generated schedules per class

📄 Export to PDF: Export timetable to a formatted PDF

🔍 Entity Browser: Buttons to view detailed teacher/class/subject/room data

✅ PDF Export Example
After generation, click on "📄 Export as PDF" to save the final timetable to your local system.

## ❗ Error Handling
Skipped subjects due to constraints are shown in the output

Break period is validated to be within range

Users are prompted on invalid inputs via GUI messages
## Summary
TimelyAI is a well-designed, complete academic scheduling system that balances usability with functional depth. For a university or school setup, it provides everything needed to generate fair, efficient, and printable timetables. With minor improvements and future enhancements (AI/ML, web version), it has the potential to become a full-scale deployable tool.
