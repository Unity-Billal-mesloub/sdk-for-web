```javascript
import { Client, Account } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const account = new Account(client);

const result = await account.updatePushTarget({
    targetId: '<TARGET_ID>',
    identifier: '<IDENTIFIER>'
});

console.log(result);
```