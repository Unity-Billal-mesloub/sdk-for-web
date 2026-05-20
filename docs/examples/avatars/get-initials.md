```javascript
import { Client, Avatars } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const avatars = new Avatars(client);

const result = avatars.getInitials({
    name: '<NAME>', // optional
    width: 0, // optional
    height: 0, // optional
    background: '' // optional
});

console.log(result);
```