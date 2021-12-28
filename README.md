# `action-deploy-jdk-package` - **Github Action**

This action deploy maven package

## Input

| Name                         | Description                                 | Required | Default |
|------------------------------|---------------------------------------------|----------|---------|
| `jdk-version`                | The jdk version to use                      | ✗        | 15      |
| `jdk-distribution`           | The jdk distribution to use                 | ✗        | adopt   |
| `server-id`                  | Value of repository/id field of the pom.xml | ✗        | ossrh   |
| `server-username`            | Deploy repository username                  | ✓        | 
| `server-password`            | Deploy repository password                  | ✓        |
| `deploy-secret-key`          | Repository deploy secret key                | ✓        |
| `deploy-secret-key-password` | Repository deploy secret key password       | ✓        |

## Example Workflow File

```yaml
name: Deploy maven package

on: [ master ]

jobs:
  deploy:
    runs-on: ubuntu-latest
      steps:
        uses: valitydev/action-deploy-jdk-package@v1.0.0
```
