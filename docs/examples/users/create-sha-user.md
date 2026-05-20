```javascript
import { Client, Users, PasswordHash } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const users = new Users(client);

const result = await users.createSHAUser({
    userId: '<USER_ID>',
    email: 'email@example.com',
    password: 'password',
    passwordVersion: PasswordHash.Sha1, // optional
    name: '<NAME>' // optional
});

console.log(result);
```