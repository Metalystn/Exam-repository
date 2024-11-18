### Exam Registration
This is a core feature. This is because registering for exams is an important part of the course completion process for students.

### Feature: Registering for an exam
As a student, I need to register to an exam so that I can pass the course.

### Feature breakdown
- Student logs in.
- The system authenticates student.
  - If the authentication fails, it requires the student to log in again.
  - If the authentication is successful, the system displays the students' home page.
- The student opens the registration interface.
- The system retrieves the list of subjects the student is registered for.
- The student selects a list of the subjects they are registered for.
- Optionally, the student can choose the teacher that handles the terms for those subjects.
- The system shows a list of exam terms that match the selected subject and teacher.
- The student chooses one exam term to register for.
- The system checks if the student is allowed to register for the selected exam (e.g., prerequisites, registration deadlines).
- If the student is allowed:
  - the system registers the student for the exam and confirms the registration.
  - The system updates the student’s exam registration status.
  - The student receives a confirmation of the registration.
- If the student is not allowed:
  - the system prevents them from registering for the exam.
  - The student receives a clear notification explaining why they are not allowed (e.g. prerequisites, registration deadlines).
- Optionally, the student can deregister from the term.
- The system tracks the deadline for deregistration and prevents deregistration after the specified deadline.
- The exam registration status is visible to both students and instructors.

### Responsibilities

### Student Authentification
- Provide functional log in page.
- Provide secure authentication process to the student.

#### Registration data collection responsibilities
- Display a list of subjects the student is registered for.
- Optionally, allow students to filter exam terms by teacher.
- Show a list of available exam terms based on subject and teacher selection.
- Validate that the student meets the prerequisites and is allowed for the exam.
- Ensure data related to exam dates, times, and registration slots is up-to-date.
- Allow students to select their exam term from the list.

#### Exam registration process responsibilities
- Verify that student meets the requirements to take the exam.
- Record the students registration for the selected exam.
- Verify that exam capacity is not exceeded.
- Allow students to deregister from exams before the deadline.

#### Confirmation and notification responsibilities
- Provide immediate feedback to the student about the success or failure of their registration.
- Send an email or notification to the student confirming the registration.
- Display registered exams in the students exam dates dashboard.

#### Deregistration responsibilities
- Enable the student to deregister from an exam before the deadline.
- Ensure that deregistered slots are made available for other students.
  
