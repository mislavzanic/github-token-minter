# GitHub Token Minter

Service built to act as a GitHub App and produce tokens that can be used for cross repo access.


# Configuration

## Supported env vars

ENV VAR name                       | Description
-----------------------------------| -----------
GITHUB_APP_ID                      | GitHub App Id created following the app creation instructions at https://docs.github.com/en/developers/apps/building-github-apps/creating-a-github-app
GITHUB_PRIVATE_KEY                 | Private key generated as part of the GitHub App creation
GITHUB_INSTALL_ID                  | GitHub Installation Id generated by installing the app via https://docs.github.com/en/developers/apps/managing-github-apps/installing-github-apps
GITHUB_JKWS_URL                    | JWKS endpoint to use to verify JWTs from GitHub. Defaults to `https://token.actions.githubusercontent.com/.well-known/jwks`
GITHUB_ACCESS_TOKEN_URL_PATTERN    | Access token url to be used for calls to https://docs.github.com/en/rest/apps/installations. *Must contain a single `%s` representing the `installation id`. Defaults to `https://api.github.com/app/installations/%s/access_tokens`
PORT                               | Port to run the service on. Defaults to `8080`
CONFIGS_DIR                        | Location of repository configuration files. Defaults to `configs`
