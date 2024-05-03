graph TD

classDef blue fill:#faf9f9,stroke:#888,stroke-width:2px;

DSK(Desktop)-->GUI
GUI[Whirlpool-gui] -->|rest|CLIAPI{cli-api}
DEV(REST API)-->|rest|CLIAPI

CLIAPI -->CLI[Whirlpool-cli]
CMD(Command-line)-->|java -jar|CLI

CLI-->CLIENT[Whirlpool-client]
WALLET(Android)-->|gradle|CLIENT
JAVA(Java)-->|maven|CLIENT
class DSK,DEV,JAVA,CMD,WALLET blue
