# React GCP Deploy Example

Build your app to docker image, publish and deploy on GCP [Cloud Run](https://console.cloud.google.com/run).

GCP Cloud Run: [DEMO](https://create-react-app-2w7qqxwz2q-uc.a.run.app/)

1. Create GCP [project](https://console.cloud.google.com/projectcreate)

2. Creating [service account keys](https://cloud.google.com/iam/docs/creating-managing-service-account-keys)

3. Download json key look like this:

```json
{
  "type": "service_account",
  "project_id": "project-id",
  "private_key_id": "key-id",
  "private_key": "-----BEGIN PRIVATE KEY-----\nprivate-key\n-----END PRIVATE KEY-----\n",
  "client_email": "service-account-email",
  "client_id": "client-id",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://accounts.google.com/o/oauth2/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "https://www.googleapis.com/robot/v1/metadata/x509/service-account-email"
}
```

4. Create Github Secrets

    - GCP_SA_EMAIL
    - GCP_SA_KEY (paste json file)
    - GCP_PROJECT_ID

5. Add `main.yml` to your project

6. Add `Dockerfile` to your project

7. Push your project to Github repo

6. Run Github Actions

8. Add `allUsers` as a member and assign it the role of "Cloud Run Caller"

9. Check out the website