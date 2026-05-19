```javascript
import { Client, Backups } from "appwrite";

const client = new Client()
    .setEndpoint('https://<REGION>.cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<YOUR_PROJECT_ID>'); // Your project ID

const backups = new Backups(client);

const result = await backups.deletePolicy({
    policyId: '<POLICY_ID>'
});

console.log(result);
```
