# User Story
**As a manager, I need to create a report of results so that people registering for a particular class can see metrics like pass rate, fail rate, and more.**

## Feature Breakdown

1. **The manager logs in.**

2. **The system authenticates manager.**
   - If the authentication fails, it requires the manager to log in again.
   - If the authentication is successful, the system displays the managers home page.

3. **The manager opens the results reporting interface.**
   
4. **The system retrieves historical result data for the selected class.**
   
5. **The system calculates relevant metrics:**
   - Pass rate
   - Fail rate
   - Average score
   - Distribution of grades or other relevant statistics

6. **The system displays these metrics in a report format to the manager:**
   - Summary metrics (pass/fail rates, average scores, etc.)
   - Visuals or charts for quick insights (e.g., bar charts, pie charts)

7. **The manager can perform the following actions:**
   - **Save the report**: Store the generated report in the centralized database for future reference.
   - **Edit specific metrics or add notes**: If needed, add commentary or clarify specific details for future viewers.
   - **Share the report**: Make the report viewable to users registering for the class, either by making it public or granting access permissions.

8. **If the manager saves the report:**
   - **The system checks for existing reports** on the same class and term to avoid duplicates.
   - **If a duplicate exists**: The system prompts the manager to confirm updating the existing report or creating a new one.
   - **If no duplicate exists**: The system saves the report in the centralized database.

9. **If the manager shares the report:**
   - The system verifies the permissions for the intended viewers (registrants or other roles).
   - The system updates access rights and links the report to the registration interface for the relevant class.

## Responsibility of the Feature

- **Manager Authentification**
  - Provide functional log in page.
  - Provide secure authentication process to the manager. 

- **Data Collection Responsibility**
  - Integrate with the centralized database to retrieve past results.
  - Ensure that data is retrieved accurately and includes necessary fields like grades, dates, and student IDs.

- **Data Processing Responsibility**
  - Calculate pass rates, fail rates, and other metrics.
  - Ensure that metrics are calculated accurately and represent the data clearly.

- **Data Writing Responsibility**
  - Store the generated report in the centralized database.
  - Allow updates or edits to existing reports.
  - Ensure data is transmitted correctly and maintains integrity.

- **Data Display Responsibility**
  - Present results metrics in a user-friendly, visually appealing format.
  - Ensure the report is accessible to designated viewers when shared.

- **Data Conflict Responsibility**
  - Avoid duplicate reports by checking existing records for the same class and term.
  - Ensure report updates are conflict-free with existing data in the database.
