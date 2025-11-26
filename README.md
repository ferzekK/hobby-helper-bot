```mermaid
erDiagram
    USER ||--o{ HABIT : has
    USER ||--o{ TASK : has
    HABIT ||--o{ HABIT_LOG : generates
    TASK ||--o{ TASK_LOG : generates

    USER {
        username
        created_at
    }

    HABIT {
        user
        title
        schedule
        created_at
    }

    HABIT_LOG {
        habit
        date
        done
    }

    TASK {
        user
        title
        deadline
        priority
    }

    TASK_LOG {
        task
        completed_at
    }
```
