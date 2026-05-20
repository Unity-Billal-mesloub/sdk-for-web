```javascript
import { Client, Messaging } from "appwrite";

const client = Client.fromJWT({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    jwt: '<YOUR_JWT>' // Your secret JSON Web Token
});

const messaging = new Messaging(client);

const result = await messaging.deleteSubscriber({
    topicId: '<TOPIC_ID>',
    subscriberId: '<SUBSCRIBER_ID>'
});

console.log(result);
```