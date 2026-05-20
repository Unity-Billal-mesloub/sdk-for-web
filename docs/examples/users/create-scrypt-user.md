```javascript
import { Client, Users } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const users = new Users(client);

const result = await users.createScryptUser({
    userId: '<USER_ID>',
    email: 'email@example.com',
    password: 'password',
    passwordSalt: '<PASSWORD_SALT>',
    passwordCpu: null,
    passwordMemory: null,
    passwordParallel: null,
    passwordLength: null,
    name: '<NAME>' // optional
});

console.log(result);
```