# Hands-on Guide: Using GitHub REST API for Documentation Projects

### Prerequisites

Before using the GitHub REST API, ensure you have:

* A __GitHub account__
* A __GitHub personal access token (PAT)__ with the required scopes (`repo` for private repositories, `public_repo` for public repositories)
* A REST API client like Postman or command-line tools like cURL

## 1. Authenticating with GitHub API

To authenticate API requests, use your __Personal Access Token (PAT)__ in the `Authorization` header.

#### Example cURL Request:

```sh
curl -H "Authorization: token YOUR_PERSONAL_ACCESS_TOKEN" \
     -H "Accept: application/vnd.github.v3+json" \
     https://api.github.com/user
```

## 2. Creating a New Repository

This API call creates a new repository under your GitHub account.

#### Endpoint

POST `https://api.github.com/user/repos`

#### Required Headers

```json
{
  "Authorization": "token YOUR_PERSONAL_ACCESS_TOKEN",
  "Accept": "application/vnd.github.v3+json"
}
```

#### Request Body Parameters

|-----|-----|-----|
|Parameter|Type|Description|
|name|string|Repository name|
|description|string|Short description of the repository|
|private|boolean|`true` for a private repo, `false` for public|


#### Example Request (cURL)

```sh
curl -X POST https://api.github.com/user/repos \
     -H "Authorization: token YOUR_PERSONAL_ACCESS_TOKEN" \
     -H "Accept: application/vnd.github.v3+json" \
     -d '{
       "name": "documentation-project",
       "description": "A repository for technical documentation",
       "private": false
     }'
```

#### Expected Response

```json
{
  "id": 123456,
  "name": "documentation-project",
  "full_name": "your-username/documentation-project",
  "private": false,
  "html_url": "https://github.com/your-username/documentation-project"
}
```

## 3. Creating a New Branch

To create a branch, first fetch the latest commit SHA of the branch you want to branch from, then create a new branch.

### Step 1: Get Latest Commit SHA of `main`

__GET__ `https://api.github.com/repos/your-username/documentation-project/git/ref/heads/main`

#### Example Request (cURL)

```sh
curl -H "Authorization: token YOUR_PERSONAL_ACCESS_TOKEN" \
     -H "Accept: application/vnd.github.v3+json" \
     https://api.github.com/repos/your-username/documentation-project/git/ref/heads/main
```

#### Expected Response

```json
{
  "ref": "refs/heads/main",
  "node_id": "MDM6UmVmMTI3NjM1MjEwOnJlZnMvaGVhZHMvbWFpbiIs
  "object": {
    "sha": "f5a5a608d89938b3ff6bc8dc27e8450b6f74c3f2"
  }
}
```

### Step 2: Create a New Branch Using the SHA

__POST__ `https://api.github.com/repos/your-username/documentation-project/git/refs`

#### Request Body

```json
{
  "ref": "refs/heads/new-feature",
  "sha": "f5a5a608d89938b3ff6bc8dc27e8450b6f74c3f2"
}
```

#### Example Request (cURL)

```sh
curl -X POST https://api.github.com/repos/your-username/documentation-project/git/refs \
     -H "Authorization: token YOUR_PERSONAL_ACCESS_TOKEN" \
     -H "Accept: application/vnd.github.v3+json" \
     -d '{
       "ref": "refs/heads/new-feature",
       "sha": "f5a5a608d89938b3ff6bc8dc27e8450b6f74c3f2"
     }'
```

#### Expected Response

```json
{
  "ref": "refs/heads/new-feature",
  "node_id": "MDM6UmVmMTI3NjM1MjEwOnJlZnMvaGVhZHMvbmV3LWZlYXR1cmUi",
  "object": {
    "sha": "f5a5a608d89938b3ff6bc8dc27e8450b6f74c3f2"
  }
}
```

## Summary

  * Authenticate using a Personal Access Token.
  * Create a new repository for documentation using POST /user/repos.
  * Fetch the latest commit SHA of the main branch.
  * Create a new branch using POST /repos/{owner}/{repo}/git/refs.

This guide helps you automate and manage GitHub repositories for technical documentation using the REST API. 🚀