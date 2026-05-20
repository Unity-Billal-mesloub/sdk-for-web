```javascript
import { Client, Presences, Permission, Role } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const presences = new Presences(client);

const result = await presences.updatePresence({
    presenceId: '<PRESENCE_ID>',
    userId: '<USER_ID>',
    status: '<STATUS>', // optional
    expiresAt: '2020-10-15T06:38:00.000+00:00', // optional
    metadata: {}, // optional
    permissions: [Permission.read(Role.any())], // optional
    purge: false // optional
});

console.log(result);
```