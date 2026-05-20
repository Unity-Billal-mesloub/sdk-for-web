```javascript
import { Client, Messaging } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const messaging = new Messaging(client);

const result = await messaging.createSendgridProvider({
    providerId: '<PROVIDER_ID>',
    name: '<NAME>',
    apiKey: '<API_KEY>', // optional
    fromName: '<FROM_NAME>', // optional
    fromEmail: 'email@example.com', // optional
    replyToName: '<REPLY_TO_NAME>', // optional
    replyToEmail: 'email@example.com', // optional
    enabled: false // optional
});

console.log(result);
```