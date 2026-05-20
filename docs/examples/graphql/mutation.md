```javascript
import { Client, Graphql } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const graphql = new Graphql(client);

const result = await graphql.mutation({
    query: {}
});

console.log(result);
```