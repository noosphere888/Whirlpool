sequenceDiagram
    autonumber
    Note over Client,Server: << WEBSOCKET >>

    Server -->>+Client: RegisterOutputMixStatusNotification
    Note left of Client: Registering output...

    Note over Client / alt. identity,Server: << REST >> from alternate identity
    Client / alt. identity->>Server: POST /rest/registerOutput [RegisterOutputRequest]
    Note left of Client: Registered output

    Note over Client,Server: ... Wait for peers
