graph TD

classDef ext fill:#faf9f9,stroke:#888,stroke-width:2px;

GUI[Whirlpool-gui] -->|rest api|CLI[Whirlpool-cli]
CLI -->|maven|CLIENT[Whirlpool-client]

CLIENT -->|websocket + rest|PROTOCOL{Whirlpool-protocol}
CLIENT -->|maven|EXTLIBJ[ExtLibJ / BitcoinJ]

PROTOCOL -->SERVER[Whirlpool-server]

class EXTLIBJ ext
