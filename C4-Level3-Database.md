# Database Diagram

## Components

### 1. Data Storage Layer
- **Purpose**: Core repository for all system data, including students, courses, exams, grades, rooms, and reports.
- **Entities/Tables**:
  - **Students Table**: Stores student records, including personal details and ids.
  - **Courses Table**: Contains information about each course, including course codes and descriptions.
  - **Exams Table**: Details each exam, including dates, associated courses, and room assignments.
  - **Grades Table**: Stores grades assigned to students for specific courses and exams.
  - **Rooms Table**: Contains information on room capacities, locations, and schedules.
  - **Reports Table**: Stores statistical data.
- **Relationships**: Primary keys, foreign keys, and integrity constraints across tables to maintain data consistency.
- **Indexes**: Uses indexes on frequently queried columns (e.g., student ID, course code).

### 2. Transaction Manager
- **Purpose**: Manages transactions to ensure data consistency and compliance with ACID properties.
- **Components**:
  - **Transaction Logger**: Logs all transaction states, capturing "begin," "commit," and "rollback" points for rollbacks if needed.
  - **Concurrency Control**: Manages access to data across concurrent transactions to avoid conflicts (e.g., locking mechanisms).
  - **Commit/Rollback Manager**: Finalizes transactions by either committing or rolling back changes based on transaction success.
- **Interactions**:
  - Works with backend services, especially critical actions like credit awarding, grading, and registration.
  - Ensures data consistency by relating with the Data Storage Layer during data operations.

### 3. Backup and Recovery Module
- **Purpose**: Maintains data integrity and availability by performing backups and enabling recovery options.
- **Components**:
  - **Backup Scheduler**: Automates regular database backups.
  - **Backup Storage**: Stores backup files securely, typically in a separate location.
  - **Recovery Engine**: Makes restoration of data in case of data loss or corruption.
- **Interactions**:
  - **Data Storage Layer**: Creates and stores backups.
  - **Transaction Manager**: Relates with the Transaction Manager during recovery to ensure transactions are correctly committed or rolled back.

## Relationships and Labels

1. **Data Storage Layer to Transaction Manager**
   - **Label**: “Data Access & Modifications”
   - **Description**: The Transaction Manager interacts with the Data Storage Layer to commit or roll back data changes.

2. **Data Storage Layer to Backup and Recovery Module**
   - **Label**: “Backup & Restore Operations”
   - **Description**: The Backup and Recovery Module periodically backs up data and can restore data to the Data Storage Layer if needed.

3. **Transaction Manager to Data Storage Layer**
   - **Label**: “Transactional Data Operations”
   - **Description**: The Transaction Manager ensures that all data-related operations in the Data Storage Layer follow the ACID properties.

4. **Transaction Manager to Backup and Recovery Module**
   - **Label**: “Transaction Consistency during Backup/Recovery”
   - **Description**: Coordinates to ensure data consistency during backups and recovery operations.

5. **Backup and Recovery Module to Data Storage Layer**
   - **Label**: “Data Restoration”
   - **Description**: Allows the Backup and Recovery Module to restore data directly to the Data Storage Layer during recovery.

