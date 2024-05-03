sequenceDiagram
    autonumber
    Note over Client,Server: << WEBSOCKET >>

    Server-->>Client: ConfirmInputMixStatusNotification

    Note left of Client: Trying to join a mix...
    Client ->>+Server: /ws/confirmInput [ConfirmInputRequest]
    Server -->>-Client: ConfirmInputResponse
    Note left of Client: Joined a mix!

    Note over Client,Server: ... Wait for enough peers
