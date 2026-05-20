```javascript
import { Client, Project, ProjectKeyScopes } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.createKey({
    keyId: '<KEY_ID>',
    name: '<NAME>',
    scopes: [ProjectKeyScopes.ProjectRead],
    expire: '2020-10-15T06:38:00.000+00:00' // optional
});

console.log(result);
```