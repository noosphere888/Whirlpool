sequenceDiagram
    autonumber

    Note over Client,Server: << REST >>
    Client->>+Server: GET /rest/pools

    Server-->>-Client: PoolsResponse
