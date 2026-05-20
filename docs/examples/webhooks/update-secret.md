```javascript
import { Client, Webhooks } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const webhooks = new Webhooks(client);

const result = await webhooks.updateSecret({
    webhookId: '<WEBHOOK_ID>',
    secret: '<SECRET>' // optional
});

console.log(result);
```