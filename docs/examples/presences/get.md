```javascript
import { Client, Presences } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const presences = new Presences(client);

const result = await presences.get({
    presenceId: '<PRESENCE_ID>'
});

console.log(result);
```