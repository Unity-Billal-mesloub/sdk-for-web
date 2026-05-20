```javascript
import { Client, Activities } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const activities = new Activities(client);

const result = await activities.getEvent({
    eventId: '<EVENT_ID>'
});

console.log(result);
```