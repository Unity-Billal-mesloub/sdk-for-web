```javascript
import { Client, Avatars, Browser } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const avatars = new Avatars(client);

const result = avatars.getBrowser({
    code: Browser.AvantBrowser,
    width: 0, // optional
    height: 0, // optional
    quality: -1 // optional
});

console.log(result);
```