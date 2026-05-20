```javascript
import { Client, Backups, BackupServices } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const backups = new Backups(client);

const result = await backups.createPolicy({
    policyId: '<POLICY_ID>',
    services: [BackupServices.Databases],
    retention: 1,
    schedule: '',
    name: '<NAME>', // optional
    resourceId: '<RESOURCE_ID>', // optional
    enabled: false // optional
});

console.log(result);
```