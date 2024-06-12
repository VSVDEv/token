# Work with GitHub personal access token


git clone https://<GITHUB_USERNAME>:<ACCESS_TOKEN>@github.com/<GITHUB_USERNAME>/<repository>.git 

git push --set-upstream https://<GITHUB_USERNAME>:<ACCESS_TOKEN>@github.com/<GITHUB_USERNAME>/<repository>.git 



https://docs.github.com/en/enterprise-server@3.9/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens

## Step 1: Generate a Personal Access Token

GitHub-Settings-Developer settings-Personal access tokens
-Generate new token-name it- scopes-

## Step 2: Configure Git to Use the Token

git config --global credential.helper '!f() { sleep 1; echo "username=git token=<TOKEN>"; }; f'

git commit -am "Test commit"
git push


