```javascript
import { Client, Messaging } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const messaging = new Messaging(client);

const result = await messaging.createTextmagicProvider({
    providerId: '<PROVIDER_ID>',
    name: '<NAME>',
    from: '+12065550100', // optional
    username: '<USERNAME>', // optional
    apiKey: '<API_KEY>', // optional
    enabled: false // optional
});

console.log(result);
```