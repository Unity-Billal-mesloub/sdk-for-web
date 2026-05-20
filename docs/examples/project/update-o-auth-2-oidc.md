```javascript
import { Client, Project } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.updateOAuth2Oidc({
    clientId: '<CLIENT_ID>', // optional
    clientSecret: '<CLIENT_SECRET>', // optional
    wellKnownURL: 'https://example.com', // optional
    authorizationURL: 'https://example.com', // optional
    tokenURL: 'https://example.com', // optional
    userInfoURL: 'https://example.com', // optional
    enabled: false // optional
});

console.log(result);
```