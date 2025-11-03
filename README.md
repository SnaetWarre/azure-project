# Azure ML Project

GitHub Actions workflow for Azure Machine Learning integration.

## Setup

1. Create Azure Service Principal:
   ```bash
   az ad sp create-for-rbac -n "MLOps-SP-NS" --role Contributor \
     --scopes /subscriptions/<subID>/resourceGroups/<resourceGroupName> --json-auth
   ```

2. Add service principal JSON as GitHub secret: `AZURE_CREDENTIALS`

3. Update environment variables in workflow:
   - GROUP: Resource group name
   - WORKSPACE: Azure ML workspace name
   - LOCATION: Azure region

## Workflows

- `azure-ml.yml` - Azure ML compute operations

