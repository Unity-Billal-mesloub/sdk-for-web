```javascript
import { Client, TablesDB, Permission, Role } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const tablesDB = new TablesDB(client);

const result = await tablesDB.createTable({
    databaseId: '<DATABASE_ID>',
    tableId: '<TABLE_ID>',
    name: '<NAME>',
    permissions: [Permission.read(Role.any())], // optional
    rowSecurity: false, // optional
    enabled: false, // optional
    columns: [], // optional
    indexes: [] // optional
});

console.log(result);
```