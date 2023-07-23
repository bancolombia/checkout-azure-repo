# Checkout Azure Repo

GitHub Action which allows you to check-out an Azure Repository. At the current version, it works with an Azure token.

## Input variables

The required variables for it to work can be appreciated next.

| Variable | Descritpion | Example |
| -------- | ----------- | ------- |
| `repo_url` | Url of the Azure Repo. It is imporant to notice that this variable __must not come with the https://__ | [azure.com/owner/repo]() |
| `token` | Valid token from an Azure account. | xXyYzZ01?! |
| `username` | Username of the Azure account | john_doe |

## Usage

```yaml
- uses: bancolombia/checkout-azure-repo@v1
  with:
    # Personal access token (PAT) used to fetch the repository. 
    
    # We recommend using a service account with the least permissions necessary. Also
    # when generating a new PAT, select the least scopes necessary.
    token: xXyYzZ01?!

    #Username of the Azure account with the neccesary permissions to clone the repository
    username: john_doe

    #The repository url from the Azure domain. It mustn't come with the https
    repo_url: azure.com/owner/repo
```
