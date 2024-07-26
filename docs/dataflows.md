```mermaid
flowchart TD
    UI[User Interface]
    Server[Server\nApplication]
    Cloud{{Cloud Service}}
    DB[(Database)]

    UI -->|Data Request| Server
    Server -->|Process Data| Cloud
    Cloud -->|Store Data| DB
    DB -->|Send Data| Server
    Server -->|Response| UI
