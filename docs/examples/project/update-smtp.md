```javascript
import { Client, Project, ProjectSMTPSecure } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const project = new Project(client);

const result = await project.updateSMTP({
    host: '', // optional
    port: null, // optional
    username: '<USERNAME>', // optional
    password: '<PASSWORD>', // optional
    senderEmail: 'email@example.com', // optional
    senderName: '<SENDER_NAME>', // optional
    replyToEmail: 'email@example.com', // optional
    replyToName: '<REPLY_TO_NAME>', // optional
    secure: ProjectSMTPSecure.Tls, // optional
    enabled: false // optional
});

console.log(result);
```