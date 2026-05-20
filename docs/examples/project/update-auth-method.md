```javascript
import { Client, Project, ProjectAuthMethodId } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.updateAuthMethod({
    methodId: ProjectAuthMethodId.EmailPassword,
    enabled: false
});

console.log(result);
```