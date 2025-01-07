 ```mermaid
sequenceDiagram
    participant PlatformHubWebhook as PlatformHubWebhook
    participant Plugin as Plugin
    participant BackendService as BackendService

    PlatformHubWebhook ->> Plugin: triggerEvent()
    activate Plugin
    Plugin ->> Plugin: onWebhookEvent()
    Plugin ->> BackendService: sendToBackend()
    BackendService -->> Plugin: receiveFromBackend()
    deactivate Plugin

    BackendService ->> Plugin: sendData()
    activate Plugin
    Plugin ->> BackendService: receiveData()
    deactivate Plugin
 ```