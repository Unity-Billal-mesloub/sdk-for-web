```javascript
import { Client, Backups } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const backups = new Backups(client);

const result = await backups.updatePolicy({
    policyId: '<POLICY_ID>',
    name: '<NAME>', // optional
    retention: 1, // optional
    schedule: '', // optional
    enabled: false // optional
});

console.log(result);
```