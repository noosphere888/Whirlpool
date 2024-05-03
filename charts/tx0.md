sequenceDiagram
    autonumber

    Note over Client,Server: << REST >>

    Note left of Client: Preview TX0...
    Client->>+Server: POST /rest/tx0 [Tx0DataRequestV2]
    Server-->>-Client: Tx0DataResponseV2

    Note left of Client: Push TX0...
    Client-->>+Server: POST /rest/tx0/push [Tx0PushRequest]
    alt success
        Server-->>-Client: PushTxResponse
    else error
        Server-->>Client: PushTxErrorResponse
    end
