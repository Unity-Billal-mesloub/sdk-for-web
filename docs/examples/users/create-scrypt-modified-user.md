```javascript
import { Client, Users } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const users = new Users(client);

const result = await users.createScryptModifiedUser({
    userId: '<USER_ID>',
    email: 'email@example.com',
    password: 'password',
    passwordSalt: '<PASSWORD_SALT>',
    passwordSaltSeparator: '<PASSWORD_SALT_SEPARATOR>',
    passwordSignerKey: '<PASSWORD_SIGNER_KEY>',
    name: '<NAME>' // optional
});

console.log(result);
```