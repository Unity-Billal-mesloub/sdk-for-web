```javascript
import { Client, Sites, DeploymentDownloadType } from "appwrite";

const client = Client.fromAPIKey({
    endpoint: 'https://<REGION>.cloud.appwrite.io/v1', // Your API Endpoint
    projectId: '<YOUR_PROJECT_ID>', // Your project ID
    apiKey: '<YOUR_API_KEY>' // Your secret API key
});

const sites = new Sites(client);

const result = sites.getDeploymentDownload({
    siteId: '<SITE_ID>',
    deploymentId: '<DEPLOYMENT_ID>',
    type: DeploymentDownloadType.Source // optional
});

console.log(result);
```