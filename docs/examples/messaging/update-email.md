```javascript
import { Client, Messaging } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const messaging = new Messaging(client);

const result = await messaging.updateEmail({
    messageId: '<MESSAGE_ID>',
    topics: [], // optional
    users: [], // optional
    targets: [], // optional
    subject: '<SUBJECT>', // optional
    content: '<CONTENT>', // optional
    draft: false, // optional
    html: false, // optional
    cc: [], // optional
    bcc: [], // optional
    scheduledAt: '2020-10-15T06:38:00.000+00:00', // optional
    attachments: [] // optional
});

console.log(result);
```