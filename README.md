# Bulk Repo Cloner for GitHub, GitLab and BitBucket

A set of bash scripts to interact with a repos from GitHub, BitBucket, and GitLab. In addition, you can use `clone-by-url` to clone repos based on any repo URL.

## `clone-by-url`

`clone-by-url` is a bash script that allows you to clone repositories from BitBucket, GitHub, or GitLab based on the provided URL. The script will automatically determine the Git service based on the provided URL and use the corresponding commands to clone the repository.

### Usage

```bash
./clone-by-url <repo_url> [target_directory]
```

- `<repo_url>`: The URL of the repository you want to clone. It can be from BitBucket, GitHub, or a GitLab instance.
- `[target_directory]` (optional): The target directory where the repository will be cloned. If not provided, the repository will be cloned to the current directory.

### Examples

Example #1:

```bash
./clone-by-url https://github.com/spekulatius
# ... clones all repos of "spekulatius"
```

Example #2:

```bash
./clone-by-url https://github.com/spekulatius/bulk-repo-cloner/blob/master/README.md
# ... clones all repos of "spekulatius"
```


## GitHub: `github-clone-public-repos`

This script allows you to clone all the public repositories from a GitHub profile. It utilizes the GitHub API to fetch repository URLs and clones them into a specified target directory or the current directory if not provided. If the repositories already exist in the target directory, the script will navigate into each directory and run `git pull` to update them.

### Usage

```bash
./github-clone-public-repos <username> [target_directory]
```

- `<username>`: The GitHub username for which you want to clone public repositories.
- `[target_directory]` (optional): The directory where you want to clone the repositories. If not provided, the current directory will be used as the target directory.

### Examples

Example #1:

```bash
./github-clone-public-repos spekulatius
# ... clones all repos of "spekulatius"
```

Example #2:

```bash
./github-clone-public-repos https://github.com/spekulatius/test/whatever/it/does/not/matter
# ... clones all repos of "spekulatius"
```


## BitBucket: `bitbucket-clone-public-repos`

This script allows you to clone all the public repositories from a BitBucket profile. It utilizes the BitBucket API to fetch repository URLs and clones them into a specified target directory or the current directory if not provided. If the repositories already exist in the target directory, the script will navigate into each directory and run `git pull` to update them.

### Usage

```bash
./bitbucket-clone-public-repos <username> [target_directory]
```

- `<username>`: The BitBucket username for which you want to clone public repositories.
- `[target_directory]` (optional): The directory where you want to clone the repositories. If not provided, the current directory will be used as the target directory.


## GitLab: `gitlab-clone-public-repos`

This script allows you to clone all the public repositories from a GitLab instance. It requires you to provide the GitLab instance URL, username, and optionally a target directory. If you are referring to the regular GitLab use `gitlab.com` as instance URL. The script uses the GitLab API to fetch repository URLs from the provided instance URL and clones them into the specified target directory or the current directory if not provided. If the repositories already exist in the target directory, the script will navigate into each directory and run `git pull` to update them.

### Usage

```bash
./gitlab-clone-public-repos <instance_url> <username> [target_directory]
```

- `<instance_url>`: The URL of the GitLab instance from which you want to clone public repositories.
- `<username>`: The GitLab username for which you want to clone public repositories.
- `[target_directory]` (optional): The directory where you want to clone the repositories. If not provided, the current directory will be used as the target directory.

### Examples

Example #1:

```bash
./gitlab-clone-public-repos gitlab.com/gabrielengel_gl/
# ... clones all repos of "gabrielengel_gl"
```

Example #2:

```bash
./gitlab-clone-public-repos https://github.com/gabrielengel_gl/test/whatever/it/does/not/matter
# ... clones all repos of "gabrielengel_gl"
```