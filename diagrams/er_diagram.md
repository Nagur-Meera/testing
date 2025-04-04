# Entity Relationship (ER) Diagram

```mermaid
erDiagram
    USER ||--o{ PROFILE : has
    USER ||--o{ MESSAGE : sends
    USER ||--o{ PROGRAM_ASSIGNMENT : has
    PROGRAM ||--o{ SECTION : contains
    SECTION ||--o{ STUDENT : enrolls
    FACULTY ||--o{ PROGRAM : manages
    PROFILE {
        string studentId
        string college
        string branch
        string department
        string currentYear
        string currentSemester
        float currentGPA
        string profilePic
        string timetable
        string coursesTable
    }
    USER {
        string id
        string name
        string email
        string password
        string role
    }
    PROGRAM {
        string id
        string title
        string description
        string facultyId
    }
    SECTION {
        string id
        string name
        string programId
    }
    MESSAGE {
        string id
        string senderId
        string receiverId
        string content
        datetime timestamp
    }
} 