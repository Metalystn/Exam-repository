# Context Diagram

## Exam Management System

### External Actors:
- **Teacher**: 
  - Manages exam-related tasks such as awarding credits and assigning grades.
- **Student**: 
  - Registers for exams and views results.
- **Manager**: 
  - Oversees administrative tasks like room management and report generation.

### External Systems:
- **Notification System**: 
  - Sends alerts and notifications (e.g., exam registration confirmation, grade announcements).
- **Database**: 
  - Stores all relevant exam, student, and course information.

# Container Diagram

## Containers in the Exam Management System

### 1. Web Application
- **Purpose**: The user interface for interacting with the system.
- **Responsibilities**:
  - **Teacher Portal**: Manage credits, grades, and courses.
  - **Student Portal**: Register for exams, view grades and results.
  - **Manager Portal**: Manage room registration, write reports.
- **Interactions**: Connects to backend microservices for core functionality.

### 2. Backend Microservices
- **Purpose**: Handles core business logic of the system.
- **Services**:
  - **Credit Awarding Service**:
    - Awards credits based on student data and conditions.
    - Updates records in the database and triggers notifications.
  - **Grading Service**:
    - Manages grade entry, calculation, and publishing.
    - Sends notifications to students once grades are published.
  - **Exam Registration Service**:
    - Handles student exam registration, deregistration, and validation.
    - Checks capacity limits and prerequisites.
  - **Room Management Service**:
    - Manages room availability and scheduling for exams.
    - Updates and validates room allocations.
  - **Statistical Reporting Service**:
    - Generates reports for managers on exam performance, pass/fail rates, etc.
  
### 3. Database
- **Purpose**: Stores data required by all the services.
- **Responsibilities**:
  - Holds student records, course data, exam schedules, grades, and room allocations.

### 4. Notification Service
- **Purpose**: Sends notifications triggered by system events.
- **Responsibilities**:
  - Sends email and SMS alerts (e.g., exam registration confirmation, credit awards, grade publication).
  - Logs notification statuses (sent, delivered, failed) for auditing.
