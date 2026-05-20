```javascript
import { Client, Teams } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const teams = new Teams(client);

const result = await teams.getMembership({
    teamId: '<TEAM_ID>',
    membershipId: '<MEMBERSHIP_ID>'
});

console.log(result);
```