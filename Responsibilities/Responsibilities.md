### Awarding Credits Responsibilities

#### Data Collection Responsibilities:
**Database Integration:**
- Fetch the list of courses the teacher is teaching using a query from the SIS database.
- Retrieve the list of enrolled students for the selected course.
- If applicable, retrieve midterm/quiz results for each student.

**Condition Checks:**
- Verify if the student has met the conditions (grades, attendance, etc.) for receiving the credit.

#### Data Display Responsibilities:
- Display the list of courses and students in the teacher’s dashboard.
- Display student grades (if applicable) and provide a clear action button ("Award Credit").

#### Error Handling and Validation Responsibilities:
- Ensure that the system checks if the student meets the credit conditions before allowing the teacher to proceed.
- Handle the teacher's input on the confirmation dialog and proceed accordingly (yes/no).

#### System Communication Responsibilities:
- Integrate with email/SMS APIs or internal notification services to send automated messages to students once credit is awarded.
- Ensure that notification status (sent, delivered, failed) is logged and visible to the teacher if needed.
- Use transactional operations in the database to ensure that awarding credit and sending student notifications are atomic actions (either both succeed, or neither does).

---

### Awarding Grades Responsibilities

#### Data Handling:
- **Secure and Accurate Grade Input:**  
Ensure that grades are entered accurately and stored securely in the centralized database.

#### Automated Calculations:
- For objective questions, the system should ensure that calculations are correct and in line with grading rubrics.

#### User Interface:
- **Grade Entry and Feedback Interface:**  
Provide a simple, intuitive interface for teachers to enter grades and feedback, with clear navigation and support for both manual and automated grading processes.

#### Notifications and Communication:
- **Student Notification:**  
Once grades are published, the system should notify students immediately. Students should be able to view their grades, feedback, and performance insights in their personal dashboards.

#### Analytics and Reporting:
- **Grade Analysis:**  
Offer teachers insights into class-wide performance, helping them make informed decisions about future teaching strategies or exam difficulty.

---

### Exam Registration Responsibilities

#### Registration Data Collection Responsibilities:
- Display a list of subjects the student is registered for.
- Optionally, allow students to filter exam terms by teacher.
- Show a list of available exam terms based on subject and teacher selection.
- Validate that the student meets the prerequisites and is allowed to register for the exam.
- Ensure data related to exam dates, times, and registration slots is up-to-date.
- Allow students to select their exam term from the list.

#### Exam Registration Process Responsibilities:
- Verify that the student meets the requirements to take the exam.
- Record the student's registration for the selected exam.
- Verify that exam capacity is not exceeded.
- Allow students to deregister from exams before the deadline.

#### Confirmation and Notification Responsibilities:
- Provide immediate feedback to the student about the success or failure of their registration.
- Send an email or notification to the student confirming the registration.
- Display registered exams in the student's exam dates dashboard.

#### Deregistration Responsibilities:
- Enable the student to deregister from an exam before the deadline.
- Ensure that deregistered slots are made available for other students.

---

### Registration of Rooms Responsibilities

#### Data Collection Responsibilities:
- Integrate with a centralized database.
- Ensure transmission from the centralized database to the machine.
- Ensure that the transmitted data is syntactically correct.

#### Data Writing Responsibilities:
- Integrate with the centralized database.
- Ensure that the user has access to edit the information.
- Ensure transmission from the machine to the centralized database.
- Ensure that the transmitted data is syntactically correct.

#### Data Display Responsibilities:
- Display the information on the teacher's monitor.

#### Data Conflict Responsibilities:
- Ensure that the primary key of the data is not duplicated.

---

### Viewing Results Responsibilities

#### Security and Privacy Responsibility:
- Ensure that the student's exam results are only accessible to the authorized student.
- Implement authentication and authorization mechanisms to prevent unauthorized access to sensitive information.

#### Data Display Responsibility:
- Display results on the student’s screen.
- Clearly indicate whether the student has passed or failed, with additional feedback if available.

---

### Statistical Report Responsibilities

#### Data Collection Responsibility:
- Integrate with the centralized database to retrieve past results.
- Ensure that data is retrieved accurately and includes necessary fields like grades, dates, and student IDs.

#### Data Processing Responsibility:
- Calculate pass rates, fail rates, and other metrics.
- Ensure that metrics are calculated accurately and represent the data clearly.

#### Data Writing Responsibility:
- Store the generated report in the centralized database.
- Allow updates or edits to existing reports.
- Ensure data is transmitted correctly and maintains integrity.

#### Data Display Responsibility:
- Present results metrics in a user-friendly, visually appealing format.
- Ensure the report is accessible to designated viewers when shared.

#### Data Conflict Responsibility:
- Avoid duplicate reports by checking existing records for the same class and term.
- Ensure report updates are conflict-free with existing data in the database.
