```javascript
import { Client, Sites, TemplateReferenceType } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const sites = new Sites(client);

const result = await sites.createTemplateDeployment({
    siteId: '<SITE_ID>',
    repository: '<REPOSITORY>',
    owner: '<OWNER>',
    rootDirectory: '<ROOT_DIRECTORY>',
    type: TemplateReferenceType.Branch,
    reference: '<REFERENCE>',
    activate: false // optional
});

console.log(result);
```