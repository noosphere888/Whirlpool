sequenceDiagram
    autonumber
    Note over Client,Server: << WEBSOCKET >>

    Note left of Client: Connecting...
    Client-->>+Server: connect /ws/connect
    Client->>+Server: subscribe /private/reply (header: $poolId)
    Server -->>-Client: SubscribePoolResponse

    Note left of Client: Registering input...
    Client->>Server: /ws/registerInput [RegisterInputRequest]
    Note left of Client: Waiting for a mix...

    Note over Client,Server: ... Wait for being invited to mix
