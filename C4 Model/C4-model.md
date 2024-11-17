## Context (level 1):
The Exam System is at the center.

### External actors:
- Teacher: Manages exam-related tasks such as awarding credits and assigning grades.
- Student: Registers for exams and views results.
- Manager: Oversees administrative tasks like room management and report generation.

### External systems:
- Notification System: Sends alerts and notifications (e.g., exam registration confirmation, grade announcements).
- Database: Stores all relevant exam, student, and course information, allowing the system to quickly access and update data as needed.

---

## Containers (level 2):

### Web Application (Teacher/Student/Manager Portals):
#### Responsibilities:
- Teachers: Manage credits, grades.
- Students: Register for exams, view results.
- Managers: Handle room registration, generate reports.

### Backend API:
#### Responsibilities:
- Core logic for credits, grading, registration, room management, reporting.
- Acts as a bridge between the web app, database, and external systems.

### Database:
#### Responsibilities:
- Stores student data, exams, grades, room availability, and reports.

### Notification System (Email/SMS Gateway):
#### Responsibilities:
- Sends notifications (credit awards, grade publications, confirmations).

---

## Components (level 3):

### Credit Awarding Service:
#### Responsibilities:
- Manages the process of awarding course credits to students.
- Fetches student data and grades, checks conditions, and updates student records.
#### Interaction:
- Interacts with the teacher portal to collect input (grades, midterms, etc.).
- Writes updates to the database and triggers notifications to students once credits are awarded.

### Grading Service:

#### Responsibilities:
- Handles the process of assigning and calculating grades.
- Supports manual input by teachers as well as automated grading (e.g., for multiple-choice questions).
- Calculates and applies bonus points and feedback.
#### Interaction:
- Writes final grades to the database and sends notifications to students.

### Exam Registration Service:

#### Responsibilities:
- Manages student exam registrations, checks prerequisites, and validates exam slots.
- Allows deregistration within set deadlines and handles capacity restrictions.
#### Interaction:
- Interacts with the student portal and the database to update registration status and notify users.

### Room Management Service:

#### Responsibilities:
- Handles room availability and ensures that rooms are properly allocated for exams.
- Validates room capacity and handles conflicts when rooms are booked for other exams.
#### Interaction:
- Writes room availability data to the database and checks for conflicts.

### Statistical Reporting Service:

#### Responsibilities:
- Generates reports about exam pass rates, grade distributions, and other relevant metrics.
- Creates visual charts for managers to assess class performance over time.
#### Interaction:
- Retrieves historical exam data from the database and calculates statistics.

### Notification Service:

#### Responsibilities:
- Sends notifications (e.g., exam registration, credit awards, grades publication) to users via email or SMS.
#### Interaction:
- Sends messages based on trigger events from the other services and logs communication statuses in the database.
