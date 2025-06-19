## Toubleshooting

Even the pipelines can break. This section covers all the possible errors you might occur and the way to resolve it.

### 1. GitHub Actions Workflow Not Triggering

Cause -  Incorrect trigger in on: section workflow of yml:

Solution - Make sure you have the correct type as the following:

on:
    push:
         branches:
            - master


### 2. Missing denied permissions

Cause - Misssing secrets or incorrect repo permissions

Solutions - Check if required GitHub secrets (likeG H_token) are configured properly
            verify access token permissions


### 3. npm run build or yarn build fails

Cause - Missing dependencies or outdated pacakages

Solutions - Run npm install or yarn before build steps


### 4. Deployment Step Failing

Cause - Invalid deployment script or credentials.

Solution - Review deployment commands
           Check API keys, URLs, and branch configs.






