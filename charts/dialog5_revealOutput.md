sequenceDiagram
    autonumber
    Note over Client,Server: << WEBSOCKET >>

    Server -->>+Client: RevealOutputMixStatusNotification
    Note left of Client: Revealing output...
    Client->>-Server: /ws/revealOutput [RevealOutputRequest]
    Note left of Client: Revealed output

    Note over Client,Server: ... Wait for peers
    Server -->>+Client: FailMixStatusNotification
