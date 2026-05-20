```javascript
import { Client, Account } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const account = new Account(client);

const result = await account.createMagicURLToken({
    userId: '<USER_ID>',
    email: 'email@example.com',
    url: 'https://example.com', // optional
    phrase: false // optional
});

console.log(result);
```