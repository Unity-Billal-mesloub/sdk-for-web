```javascript
import { Client, Advisor } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const advisor = new Advisor(client);

const result = await advisor.getReport({
    reportId: '<REPORT_ID>'
});

console.log(result);
```