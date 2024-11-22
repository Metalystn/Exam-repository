# Viewing Room Details (Teachers)

This feature allows teachers to view information about room reservations. Without this functionality, teachers cannot access the capacity and availability of rooms, making it impossible to plan exams.

---

## User Story

As a teacher, I need to view details about room reservations so that I can plan and schedule exams appropriately.

---

## Feature Breakdown

1. **The user logs in.**

2. **The system authenticates user.**
  - If the authentication fails, it requires the user to log in again.
  - If the authentication is successful, the system displays the user's home page.

3. **The teacher opens the room details interface:**  
   - The system collects the list of rooms from the centralized database via the Data Access Layer.

4. **The system displays the list of rooms with details:**  
   - Room details include the room number, capacity, and availability.

5. **The teacher selects a specific room for more details:**  
   - The system retrieves detailed information about the selected room, such as:
     - Building location/address.
     - Time slots for which the room is reserved.
     - Remaining available capacity during specific time slots.

6. **The system displays the room's detailed information:**  
   - The teacher reviews the details to decide whether the room meets the needs for their exam.

7. **The teacher either confirms or returns to the list of rooms:**  
   - If confirmed, no other action is required.
   - If the teacher returns to the list, they can select another room to view its details.

---

## Responsibilities of the Feature

1. **User Authentification**
  - Provide functional log in page.
  - Provide secure authentication process to the user.

2. **Data Collection Responsibility:**  
   - Work with the centralized database to get room details.  
   - Ensure the system retrieves accurate and up-to-date data.  
   - Make error handling if room data retrieval fails.

3. **Data Display Responsibility:**  
   - Display room details (name, capacity, availability, etc.) on the teacher's screen.  
   - Provide a clear and user-friendly interface for navigating room information.

4. **User Interaction Responsibility:**  
   - Allow the teacher to return to the main interface at any time.

5. **Error Handling Responsibility:**  
   - Notify the teacher if there are issues retrieving room details (e.g., database connection errors).  
   - Provide fallback options, such as retrying data retrieval or displaying cached information.


