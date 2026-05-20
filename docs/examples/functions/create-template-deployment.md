```javascript
import { Client, Functions, TemplateReferenceType } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const functions = new Functions(client);

const result = await functions.createTemplateDeployment({
    functionId: '<FUNCTION_ID>',
    repository: '<REPOSITORY>',
    owner: '<OWNER>',
    rootDirectory: '<ROOT_DIRECTORY>',
    type: TemplateReferenceType.Commit,
    reference: '<REFERENCE>',
    activate: false // optional
});

console.log(result);
```