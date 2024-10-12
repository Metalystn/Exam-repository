# Awarding Grades (Teachers)

This is a core feature.The Awarding Grades feature allows teachers to assign grades to students based on their performance in exams or assignments. This feature provides an easy-to-use interface for grading, feedback submission, and the option to review and adjust grades if necessary. It supports both manual and automated grading processes and integrates with the exam management system to streamline the evaluation process.

---

## User Story

**As a** teacher, ***I need*** to award grades to students **so that** I can evaluate their work and provide them with feedback on their performance.

---

## Feature Breakdown

1. The teacher opens the grading interface.
2. The system retrieves and displays a list of students who completed the exam.
3. The teacher selects a student to grade or chooses to grade all students.
4. The teacher can either:
    - Input grades manually, or
    - Review automatically generated grades for objective questions.
5. If inputting manually:
    - a. The teacher enters the score for each section of the exam.
    - b. The teacher adds feedback or comments if needed.
6. If using automated grading:
    - a. The system calculates grades for objective questions (e.g., multiple-choice).
    - b. The teacher reviews and adjusts the grades if necessary.
7. Determine Bonus Criteria:
    - The teacher decides the reason for awarding bonus grades, such as:
        - Extra credit work
        - Outstanding performance
        - Participation
        - Bonus questions on the exam
8. Enter the Bonus Grades:
    - In the grade entry section, the teacher manually adds bonus points to the student's total score.
    - The system may offer a separate field to input bonus grades or allow the teacher to adjust the final score directly.
9. Review the Grades:
    - The teacher reviews all inputted grades and feedback to ensure accuracy.
    - Adjustments can be made at this stage if necessary.
10. The teacher submits the final grades.
11. The system publishes the grades, and students are notified via their exam dashboard.

---

## Responsibilities of feature

### Data Handling:
- Secure and Accurate Grade Input:
Ensure that grades are entered accurately and stored securely in the centralized database.

### Automated Calculations:
- For objective questions, the system should ensure that calculations are correct and in line with grading rubrics.

### User Interface:
- Grade Entry and Feedback Interface:
Provide a simple, intuitive interface for teachers to enter grades and feedback, with clear navigation and support for both manual and automated grading processes.
### Notifications and Communication:
- Student Notification:
Once grades are published, the system should notify students immediately, and they should be able to view their grades, feedback, and performance insights in their personal dashboards.
### Analytics and Reporting:
- Grade Analysis:
Offer teachers insights into class-wide performance, helping them make informed decisions about future teaching strategies or exam difficulty.