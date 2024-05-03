sequenceDiagram
    autonumber
    Note over Client,Server: << WEBSOCKET >>

    Server -->>+Client: SigningMixStatusNotification
    Note left of Client: Signing...
    Client->>-Server: /ws/signing [SigningRequest]
    Note left of Client: Signed

    Note over Client,Server: ... Wait for peers
    Server -->>+Client: SuccessMixStatusNotification
