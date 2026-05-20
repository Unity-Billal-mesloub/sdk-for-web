```javascript
import { Client, Messaging } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const messaging = new Messaging(client);

const result = await messaging.updateMsg91Provider({
    providerId: '<PROVIDER_ID>',
    name: '<NAME>', // optional
    enabled: false, // optional
    templateId: '<TEMPLATE_ID>', // optional
    senderId: '<SENDER_ID>', // optional
    authKey: '<AUTH_KEY>' // optional
});

console.log(result);
```