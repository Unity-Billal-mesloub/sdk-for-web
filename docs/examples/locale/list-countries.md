```javascript
import { Client, Locale } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const locale = new Locale(client);

const result = await locale.listCountries();


console.log(result);
```