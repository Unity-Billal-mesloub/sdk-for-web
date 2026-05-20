```javascript
import { Client, TablesDB, Permission, Role } from "appwrite";

const client = Client.from({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>' // Your project ID
});

const tablesDB = new TablesDB(client);

const result = await tablesDB.updateRow({
    databaseId: '<DATABASE_ID>',
    tableId: '<TABLE_ID>',
    rowId: '<ROW_ID>',
    data: {
        "username": "walter.obrien",
        "email": "walter.obrien@example.com",
        "fullName": "Walter O'Brien",
        "age": 33,
        "isAdmin": false
    }, // optional
    permissions: [Permission.read(Role.any())], // optional
    transactionId: '<TRANSACTION_ID>' // optional
});

console.log(result);
```