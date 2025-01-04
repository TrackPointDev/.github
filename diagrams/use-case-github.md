```mermaid
graph TD
    actorUser(User)
    subgraph System
        UC1(Create Epic in Google Sheets)
        UC2(Download GitHub App)
        UC3(Fill Out Rest of Sheet)
    end

    actorUser --> UC1
    actorUser --> UC2
    actorUser --> UC3

```