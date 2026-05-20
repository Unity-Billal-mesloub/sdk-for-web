```javascript
import { Client, Functions, DeploymentDownloadType } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const functions = new Functions(client);

const result = functions.getDeploymentDownload({
    functionId: '<FUNCTION_ID>',
    deploymentId: '<DEPLOYMENT_ID>',
    type: DeploymentDownloadType.Source // optional
});

console.log(result);
```