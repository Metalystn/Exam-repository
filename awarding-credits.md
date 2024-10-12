
# Awarding Credits (Teacher)

## User story
***As a*** teacher ***I want*** to award credits to student ***so that*** they can register for the final exam.

---

## Feature Breakdown

1. The teacher opens the exams interface in the student information system (SIS).
2. The system retrieves and displays the list of courses taught by the teacher from the database.
3. The teacher selects the relevant course to manage.
4. The system fetches and displays the list of students enrolled in the selected course.
5. The teacher chooses the student they want to review for credit assignment.
6. If the course uses midterms or quizzes:
    1. The system retrieves and displays the student's midterm and quiz results from the database.
    2. The teacher reviews the grades and determines if the student has earned sufficient points.
    3. The teacher selects the "Award Credit" button for the student.
    4. The system validates whether all conditions for awarding credit (like quiz/midterm performance) have been met.
    5. The system prompts the teacher with a confirmation dialog: _"Are you sure you want to award credit to this student?"_
        1. If the teacher selects "Yes," the system performs the following:
            1. Updates the student's record in the SIS, assigning the credit as "C".
            2. Saves the action (credit award, timestamp, teacher ID, etc.).
            3. Displays a success confirmation to the teacher: _"Credit successfully awarded."_
            4. Sends a notification to the student (via email, SMS, or the SIS notification system) informing them they have been awarded credit.
        2. If the teacher selects "No," the system aborts the action and returns to the previous page. 
7. If the course doesn’t rely on midterms/quizzes for credit awarding:
    1. The teacher manually assesses the student’s eligibility for getting the credit.
    2. The teacher repeats steps 3-5 (of the step 6) without reviewing midterm/quiz results.
---
## Responsibility of the feature

###  Data Collection Responsibilities:
**Database Integration:**
- Fetch the list of courses the teacher is teaching using a query from the SIS database.
- Retrieve the list of enrolled students for the selected course.
- If applicable, retrieve midterm/quiz results for each student.

**Condition Checks:**
- Verify if the student has met the conditions (grades, attendance, etc.) for receiving the credit.

### Data Display Responsibilities:
- Display the list of courses and students in the teacher’s dashboard.
- Display student grades (if applicable) and provide a clear action button ("Award Credit").

### Error Handling and Validation Responsibilities:
- Ensure that the system checks if the student meets the credit conditions before allowing the teacher to proceed.
- Handle the teacher's input on the confirmation dialog and proceed accordingly (yes/no).

### System Communication Responsibilities:
- Integrate with email/SMS APIs or internal notification services to send automated messages to students once credit is awarded.
- Ensure that notification status (sent, delivered, failed) is logged and visible to the teacher if needed.
- Use transactional operations in the database to ensure that awarding credit and sending student notifications are atomic actions (either both succeed, or neither does).
