# Azure Deployment

This project deploys automatically to Azure Container Apps through GitHub Actions.

## Live Resources

- Subscription: `477a9591-e616-49d0-972b-b2e53c906ad1`
- Tenant: `2204f1a7-d148-4edd-9f06-57012f973b70`
- Resource group: `myportfolio-rg`
- Container app: `myportfolio`
- Container app environment: `myportfolio-env`
- Azure Container Registry: `myportfolioregistry.azurecr.io`
- Managed identity client ID: `e2900889-8d66-4f1f-94a2-1c08e377f660`

## GitHub Actions

Workflow: `.github/workflows/deploy.yml`

On pull requests to `main`, the workflow installs dependencies, runs tests, and builds the app.

On pushes to `main`, it also:

1. Logs in to Azure using OIDC.
2. Builds and pushes a Docker image to ACR.
3. Updates the Azure Container App.
4. Verifies the deployed custom path.

## Required GitHub Secrets

Set these repository secrets in GitHub:

- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_PUBLISHABLE_KEY`
- `VITE_SUPABASE_PROJECT_ID`

The Azure OIDC identity and RBAC have already been configured for:

- Repository: `mdirfancse2023/My_Portfolio`
- Branch: `main`
- Federated credential: `github-main`
