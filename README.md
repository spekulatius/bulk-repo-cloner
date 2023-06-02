# Bulk Repo Cloner for GitHub, GitLab and BitBucket

A set of bash scripts to interact with a repos from GitHub, BitBucket, and GitLab.

## GitHub: `github-clone-public-repos`

This script allows you to clone all the public repositories from a GitHub profile. It utilizes the GitHub API to fetch repository URLs and clones them into a specified target directory or the current directory if not provided. If the repositories already exist in the target directory, the script will navigate into each directory and run `git pull` to update them.

### Usage

```bash
./github-clone-public-repos <username> [target_directory]
```

- `<username>`: The GitHub username for which you want to clone public repositories.
- `[target_directory]` (optional): The directory where you want to clone the repositories. If not provided, the current directory will be used as the target directory.


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
