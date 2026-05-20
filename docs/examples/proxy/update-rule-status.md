```javascript
import { Client, Proxy } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const proxy = new Proxy(client);

const result = await proxy.updateRuleStatus({
    ruleId: '<RULE_ID>'
});

console.log(result);
```