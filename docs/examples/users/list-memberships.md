```javascript
import { Client, Users } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const users = new Users(client);

const result = await users.listMemberships({
    userId: '<USER_ID>',
    queries: [], // optional
    search: '<SEARCH>', // optional
    total: false // optional
});

console.log(result);
```