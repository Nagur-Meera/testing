# Package Diagram

```mermaid
graph TD
    subgraph Student Management System
        A[Authentication Package]
        B[Profile Management Package]
        C[Program Management Package]
        D[Messaging Package]
        E[User Management Package]
        
        A --> B
        A --> C
        A --> D
        A --> E
        B --> C
        C --> D
    end
``` 