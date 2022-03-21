<!-- start title -->

# GitHub Action: luminsports-php-cs-fixer

<!-- end title -->

A composite action which combines php-cs-fixer, checkstyle annotation generation and automated pull-requests. See [friendsofphp/php-cs-fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer), [jwgmeligmeyling/checkstyle-github-action](https://github.com/jwgmeligmeyling/checkstyle-github-action) and [peter-evans/create-pull-request](https://github.com/peter-evans/create-pull-request).

<!-- start description -->

Use PHP-CS-Fixer via Github Action.

<!-- end description -->

<!-- start usage -->

```yaml
- uses: luminsports/github-action-php-cs-fixer@main
  with:
    # Which php-cs-fixer release to download.
    # Default: v3.7.0
    php-cs-fixer-version: ""

    # Whether to create annotations based on checkstyle results.
    # Default: true
    create-annotations: ""

    # Name for the check run to create. Default: PHP-CS-Fixer.
    # Default: PHP-CS-Fixer
    annotation-name: ""

    # Title for the check run to create. Default: PHP-CS-Fixer Results.
    # Default: PHP-CS-Fixer Results
    annotation-title: ""

    # Whether to create a pull request to fix php-cs-fixer issues.
    # Default: true
    create-pull-request: ""

    # The message to use when committing code style fixes.
    # Default: style(php-cs-fixer): Fix code-style
    commit-message: ""

    # The title of the pull request.
    # Default: Fix PHP code-style in ${{ github.ref }}
    pull-request-title: ""

    # A comma or newline separated list of assignees (GitHub usernames).
    # Default: github.actor
    pull-request-assignees: ""

    # A comma or newline separated list of reviewers (GitHub usernames) to request a
    # review from.
    # Default:
    pull-request-reviewers: ""

    # A comma or newline separated list of GitHub teams to request a review from. Note
    # that a `repo` scoped Personal Access Token (PAT) may be required.
    # Default:
    pull-request-team-reviewers: ""

    # The pull request branch name.
    # Default: php-cs-fixer/${{ github.ref }}
    pull-request-branch: ""

    # A comma or newline separated list of labels.
    # Default: php-cs-fixer
    pull-request-labels: ""
```

<!-- end usage -->

<!-- start inputs -->

| **Input**                         | **Description**                                                                                                                                    |                **Default**                | **Required** |
| :-------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------: | :----------: |
| **`php-cs-fixer-version`**        | Which php-cs-fixer release to download.                                                                                                            |                 `v3.7.0`                  |  **false**   |
| **`create-annotations`**          | Whether to create annotations based on checkstyle results.                                                                                         |                  `true`                   |  **false**   |
| **`annotation-name`**             | Name for the check run to create. Default: PHP-CS-Fixer.                                                                                           |              `PHP-CS-Fixer`               |  **false**   |
| **`annotation-title`**            | Title for the check run to create. Default: PHP-CS-Fixer Results.                                                                                  |          `PHP-CS-Fixer Results`           |  **false**   |
| **`create-pull-request`**         | Whether to create a pull request to fix php-cs-fixer issues.                                                                                       |                  `true`                   |  **false**   |
| **`commit-message`**              | The message to use when committing code style fixes.                                                                                               |   `style(php-cs-fixer): Fix code-style`   |  **false**   |
| **`pull-request-title`**          | The title of the pull request.                                                                                                                     | `Fix PHP code-style in ${{ github.ref }}` |  **false**   |
| **`pull-request-assignees`**      | A comma or newline separated list of assignees (GitHub usernames).                                                                                 |              `github.actor`               |  **false**   |
| **`pull-request-reviewers`**      | A comma or newline separated list of reviewers (GitHub usernames) to request a review from.                                                        |                                           |  **false**   |
| **`pull-request-team-reviewers`** | A comma or newline separated list of GitHub teams to request a review from. Note that a `repo` scoped Personal Access Token (PAT) may be required. |                                           |  **false**   |
| **`pull-request-branch`**         | The pull request branch name.                                                                                                                      |     `php-cs-fixer/${{ github.ref }}`      |  **false**   |
| **`pull-request-labels`**         | A comma or newline separated list of labels.                                                                                                       |              `php-cs-fixer`               |  **false**   |

<!-- end inputs -->

<!-- start outputs -->

| **Output**               | **Description**                                                                       | **Default** | **Required** |
| :----------------------- | :------------------------------------------------------------------------------------ | ----------- | ------------ |
| `checkstyle-result`      | Checkstyle report generate by php-cs-fixer                                            |             |              |
| `pull-request-number`    | The pull request number                                                               |             |              |
| `pull-request-url`       | The URL of the pull request.                                                          |             |              |
| `pull-request-operation` | The pull request operation performed by the action, `created`, `updated` or `closed`. |             |              |
| `pull-request-head-sha`  | The commit SHA of the pull request branch.                                            |             |              |

<!-- end outputs -->
