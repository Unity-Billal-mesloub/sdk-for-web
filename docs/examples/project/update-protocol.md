```javascript
import { Client, Project, ProjectProtocolId } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.updateProtocol({
    protocolId: ProjectProtocolId.Rest,
    enabled: false
});

console.log(result);
```