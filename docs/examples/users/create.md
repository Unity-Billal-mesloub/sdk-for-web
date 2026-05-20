```javascript
import { Client, Users } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const users = new Users(client);

const result = await users.create({
    userId: '<USER_ID>',
    email: 'email@example.com', // optional
    phone: '+12065550100', // optional
    password: '', // optional
    name: '<NAME>' // optional
});

console.log(result);
```