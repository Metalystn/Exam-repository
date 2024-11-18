# Viewering results (teacher)

This is an auxilary feature.
This is because while some teachers might want to view the students' progress and make changes to their exams according to the results, other need not do this.
Simply this is not mandatory

---

## User story

***As a*** teacher ***I want*** to view my student exam result ***so that*** I can follow their proggress and to make informed changes to my exams.

---

## Feature breakdown

1. The teacher opens the exams interface.
2. The system collects the list of terms that belong to the teacher.
3. The system displays the list to the teacher.
4. The teacher selects an instance of a single term.
5. The teacher makes a choice; to view a single student or to view all the results in the term.
6. If the teacher chose to view a single student result:
   - a. The system collects the list of students that has taken the selected term.
   - b. The system displays the iist to the teacher.
   - c. The teach selects a student from the list.
   - d. The system collects the information about the student's result in that term.
   - e. The system displays the result to the teacher.
7. If the teacher chose to view all the results in the exam:
   - a. The system collects the list grades that were given in the selected term.
   - b. The system displayes the list to the teacher.

---

## Resposibility of the feature

### Data collection responsibility

- Integrate with a centrelized database.
- Ensure transmission from the centrelized database to the machine.
- Ensure that the transmitted data is syntactically correct.

### Data display responsibility

- Display on the teacher's monitor.
