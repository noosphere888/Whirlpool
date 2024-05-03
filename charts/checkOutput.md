sequenceDiagram
    autonumber

    Note over Client / alt. identity,Server: << REST >> from alternate identity
    Client / alt. identity->>+Server: POST /rest/checkOutput [CheckOutputRequest]

    Server->>-Client / alt. identity: [HTTP SUCCESS 200]
