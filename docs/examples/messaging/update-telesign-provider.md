```javascript
import { Client, Messaging } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const messaging = new Messaging(client);

const result = await messaging.updateTelesignProvider({
    providerId: '<PROVIDER_ID>',
    name: '<NAME>', // optional
    enabled: false, // optional
    customerId: '<CUSTOMER_ID>', // optional
    apiKey: '<API_KEY>', // optional
    from: '<FROM>' // optional
});

console.log(result);
```