# Entity Relationship Diagram

```mermaid
erDiagram

USERS {
    uuid id PK
    string full_name
    string email
    string avatar
    string phone
    string role
    boolean active
    datetime last_login
    datetime created_at
}

PROFESSIONALS {
    uuid id PK
    string full_name
    string nickname
    string cpf
    string phone
    string email
    string city
    string state
    string notes
    string profile_image
    string instagram
    string portfolio_url
    string status
    boolean active
    datetime created_at
    uuid created_by FK
}

ROLES {
    uuid id PK
    string name
    string description
    string category
    string level
    string color
    boolean active
    datetime created_at
    uuid created_by FK
}

PROFESSIONAL_ROLES {
    uuid id PK
    uuid professional_id FK
    uuid role_id FK
}

TEAMS {
    uuid id PK
    string name
    string description
    string status
    uuid leader_id FK
    uuid created_by FK
    datetime created_at
}

TEAM_MEMBERS {
    uuid id PK
    uuid team_id FK
    uuid professional_id FK
    string status
    time start_time
    time end_time
    text notes
    boolean confirmed
    boolean signed
    datetime created_at
}

TEAM_MEMBER_ROLES {
    uuid id PK
    uuid team_member_id FK
    uuid role_id FK
    string custom_role_name
}

PRODUCTIONS {
    uuid id PK
    string name
    string description
    string client
    string production_type
    decimal budget
    string status
    string priority
    string external_contacts
    text notes
    date start_date
    date end_date
    uuid responsible_user_id FK
    uuid created_by FK
    datetime created_at
}

PRODUCTION_TEAMS {
    uuid id PK
    uuid production_id FK
    uuid team_id FK
    string location
    date event_date
    time start_time
    time end_time
    text notes
}

USERS ||--o{ TEAMS : creates
USERS ||--o{ PRODUCTIONS : creates
USERS ||--o{ PROFESSIONALS : creates
USERS ||--o{ ROLES : creates

PROFESSIONALS ||--o{ PROFESSIONAL_ROLES : has
ROLES ||--o{ PROFESSIONAL_ROLES : assigned_to

TEAMS ||--o{ TEAM_MEMBERS : contains
PROFESSIONALS ||--o{ TEAM_MEMBERS : participates

TEAM_MEMBERS ||--o{ TEAM_MEMBER_ROLES : has
ROLES ||--o{ TEAM_MEMBER_ROLES : assigned_to

PRODUCTIONS ||--o{ PRODUCTION_TEAMS : contains
TEAMS ||--o{ PRODUCTION_TEAMS : participates