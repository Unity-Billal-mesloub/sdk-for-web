```javascript
import { Client, Teams } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const teams = new Teams(client);

const result = await teams.create({
    teamId: '<TEAM_ID>',
    name: '<NAME>',
    roles: [] // optional
});

console.log(result);
```