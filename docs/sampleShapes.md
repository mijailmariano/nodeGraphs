```mermaid
flowchart TB
    subgraph 1
        direction LR
        A[(Database)] --> B[[Landing Zone]]
        B --> C{Data Lake_1}
    end
    
    subgraph 2
        direction LR
        C --> D((circle1))
        D --> E((circle2))
        E --> F
    end

    subgraph 3
        direction LR
        F{Data Lake_2}
        F --> G{{Application_1}}
        F --> H{{Application_2}}
    end

    classDef background fill:#FFFF99, stroke:#333, stroke-width:2px;  %% Light yellow background
    classDef default fill:#f9f,stroke:#333,stroke-width:2px;
    classDef database fill:#ccf,stroke:#333,stroke-width:2px;
    classDef process fill:#cfc,stroke:#333,stroke-width:2px;
    classDef decision fill:#b30,stroke:#333,stroke-width:2px;
    classDef external fill:#b30,stroke:#333,stroke-width:2px;

    class Sample background;
    class A,B,D database;
    class E database;
    class F default;
    class G process;
    class H decision;
    class I external;