```javascript
import { Client, Project } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.updateOAuth2Tradeshift({
    oauth2ClientId: '<OAUTH2_CLIENT_ID>', // optional
    oauth2ClientSecret: '<OAUTH2_CLIENT_SECRET>', // optional
    enabled: false // optional
});

console.log(result);
```