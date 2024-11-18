## Viewering results (student)  
This is a core feature. This is because all students need to know whether they passed or failed an exam in order to assess their progress and make adjustments to their studies. Therefore, this feature is mandatory for students.

# User story
As a student or a teacher, I need to view the results of an exam so that I can see whether a student pass or fail.

## Feature breakdown
- The user logs in to the system.
- The systems authinticates the user.
  - If the authintication fails, the system requires the user to retry logging in.
  - If the authintication is successful, th systems displayed the user's home page.
- The user opens the exam results interface.
- If the user is a student:
  - The system collects the list of exams across all the courses the student has taken.
  - The system displays a list of exam results, grouped by course, so the student can see all their results at once.
  - Each exam result shows the course name, and whether the student passed or failed.
  - Optionally, the student can expand any exam result to view a detailed breakdown of their score.
- If the user is a teacher:
  - The system collects and displayes the list of all courses that the teacher teaches.
  - The teacher selects a course from the list to review the results of.
  - The system collects and displayes the list of all students in the selected course alongside with their results.


## Responsibility of the feature  

### Login authenticity
- Ensures that the user logged in is authonticated by our system for secure communication.

### Security and Privacy Responsibility
- Ensure that the student's exam results are only accessible to the authorized student.
- Implement authentication and authorization mechanisms to prevent unauthorized access to sensitive information.

### Data display responsibility  
- Display on the student’s screen.
- Clearly indicate whether the student has passed or failed, with additional feedback if available.
