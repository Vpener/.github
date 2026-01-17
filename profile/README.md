## Vpener project

system for managing sing-box servers and clients

---
**Very early in development**


```mermaid
flowchart TD
    Client[Client]
    API[API]
    VPNHost[VPN Host]
    ConfigToml[Config.toml]
    TelegramBot[Telegram Admin Bot]
    
    Client -->|GET| API
    API -->|V2RayN Sub| Client
    
    API -->|Poll/Read| ConfigToml
    API -->|conf| VPNHost
    VPNHost -->|PUT health check| API
    
    TelegramBot -->|write| ConfigToml
    
    style VPNHost fill:#057029
    style API fill:#ff9999
    style ConfigToml fill:#7D6E51
    style TelegramBot fill:#6699cc
```

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
