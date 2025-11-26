## ER Diagram

```mermaid
erDiagram
    USER ||--o{ HABIT : has
    USER ||--o{ TASK : has
    HABIT ||--o{ HABIT_LOG : logs
    TASK ||--o{ TASK_LOG : logs

    USER {
        username
        created_at
    }

    HABIT {
        user (owner)
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
        user (owner)
        title
        deadline
        priority
    }

    TASK_LOG {
        task
        completed_at
    }

```
