```javascript
import { Client, Project } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.updateAndroidPlatform({
    platformId: '<PLATFORM_ID>',
    name: '<NAME>',
    applicationId: '<APPLICATION_ID>'
});

console.log(result);
```