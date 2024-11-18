# Registration of rooms (managers)

This is a core feature.
Without registered rooms with capacities and availablity the teachers cannot reserve a room for exams.

---

## User story

***As a*** manager ***I need*** to be able to register rooms available for exams ***so that*** the teachers can exam students.

---

## Feature Breakdown

1. The manager opens the rooms interface.
2. The system collects the list of rooms in which currently exam can be taken.
3. The system displays the list to the manager.
4. The manager either: selects a room, or add a new room.
5. If the manager adds a new room:
   1. The system displays necessary information on the room to be filled. (address/building, name/number of room, capacity, availablity)
   2. The teacher fills the necessary information of the new room.
   3. The system check for conflicts with other rooms. (if the primary key of a room is the same as the new room)
   4. If there is not conflict:
      The system adds the new room to the centralized database.
   6. If there is a conflict:
      1. The systems informs the manager that there is a conflict, showing the conflicted information.
      2. The teacher either: resolve the conflict or cancel the new room.
      3. If the teacher resolve the conflice return to step 5 ii.
      4. If the teacher cancel the new room return to step 1.
6. If the managers selects a room:
   1. The system collects the information of the selected room.
   2. The system displays the information of the selected room.
   3. The manager either: removes the selected room or edit information of the selected room.
   4. If the manager removes the selected room:
      1. The system checks if there are any exams in the selected room.
      2. If there are no exams: the system removes the room from the centralized database.
      3. If there are exams: the systems disallow the removal of the room.
   5. If the manager edit information of the selected room:
      1. The system check for conflicts with other rooms. (if the primary key of a room is the same as the selected room after the changes)
      2. If there is not conflict:
         The system adds the changes to the selected room to the centralized database.
      3. If there is a conflict:
         1. The systems informs the manager that there is a conflict, showing the conflicted information.
         2. The teacher either: resolve the conflict or cancel the edit of information of the selected room.
         3. If the teacher resolve the conflice return to step 5 v a.
         4. If the teacher cancel the new room return to step 6 i.

---

## Resposibility of the feature

### Data collection responsibility

- Integrate with a centralized database.
- Ensure transmission from the centralized database to the machine.
- Ensure that the transmitted data is syntactically correct.

### Data writing resposibility

- Integrate with the Centralized database.
- Ensure that the user has the access to edit the information.
- Ensure transmission from the machine to the centralized database.
- Ensure that the transmitted data is syntantically correct.

### Data display responsibility

- Display on the teacher's monitor.

### Data conflict responsibility

- Ensure that the primary key of the data is not duplicated.
