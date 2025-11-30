# GitHub Administration

> These are **NOT real questions** from the exam but quite close enough to what you can get to help you to prepare it and obtain the certification

## Skills measured

- [Support GitHub Enterprise for users and key stakeholders](#support-github-enterprise-for-users-and-key-stakeholders) (15% of the exam)
- [Manage user identities and GitHub authentication](#manage-user-identities-and-github-authentication) (20% of the exam)
- [Describe how GitHub is deployed, distributed, and licensed](#describe-how-github-is-deployed-distributed-and-licensed) (5% of the exam)
- [Manage access and permissions based on membership](#manage-access-and-permissions-based-on-membership) (20% of the exam)
- [Enable secure software development and ensure compliance](#enable-secure-software-development-and-ensure-compliance) (15% of the exam)
- [Manage GitHub Actions](#manage-github-actions) (20% of the exam)
- [Manage GitHub Packages](#manage-github-packages) (5% of the exam)

## Support GitHub Enterprise for users and key stakeholders

### What role is required to edit a team?

<details><summary>show</summary>
<p>

**Maintainer** or **admin**

</p>
</details>

### Can you have nested teams in GitHub?

<details><summary>show</summary>
<p>

Yes and it is a general practice [to use them to reflect](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams#nested-teams) the current enterprise internal's organization.

</p>
</details>

### Which formats are available when exporting audit logs?

<details><summary>show</summary>
<p>

**JSON** and **CSV**

</p>
</details>

### Which roles can be used to manage billing information?

<details><summary>show</summary>
<p>

**owner** and **billing manager**

</p>
</details>

### On GitHub Enterprise Server, which command allows you to generate a logs package to communicate to the support?

<details><summary>show</summary>
<p>

```bash
ssh -p 122 admin@hostname -- 'ghe-support-bundle -o' > support-bundle.tgz
```

</p>
</details>

## Manage user identities and GitHub authentication

### Can GitHub be synchronized with an identity provider?

<details><summary>show</summary>
<p>

Yes, for instance, Azure Active Directory but also others like ADFS, Okta, OneLogin, etc.

</p>
</details>

### What are the different methods to authenticate against GitHub?

<details><summary>show</summary>
<p>

- username/password
- PAT (Personal Access Token)
- SSH keys
- Deploy keys

</p>
</details>

### Which authentication mechanism allows users to connect using their company's credentials?

<details><summary>show</summary>
<p>

**SAML SSO**

</p>
</details>

### What are the supported 2FA (multi-factor authentication) methods?

<details><summary>show</summary>
<p>

- SMS
- TOTP app
- security keys

</p>
</details>

### Which feature allows you to synchronize exchange of user identity data between your IdP and GitHub?

<details><summary>show</summary>
<p>

**SCIM**

</p>
</details>

### What is the limit number of users in one GitHub organization?

<details><summary>show</summary>
<p>

**10000**

- Maximum number of members in a GitHub team: 5000
- Maximum number of members in a GitHub organization: 10000
- Maximum number of teams in a GitHub organization: 1500

</p>
</details>

## Describe how GitHub is deployed, distributed, and licensed

### Can an enterprise contain several organizations?

<details><summary>show</summary>
<p>

Yes.

</p>
</details>

### Are the hosted agents totally free?

<details><summary>show</summary>
<p>

Yes for public repositories. For private repositories, you have free minutes of usage offered per month.

</p>
</details>

### You plan on using GitHub Actions to build, test, and deliver your cross-platform code. Which of the following platforms will be the most expensive to use?

<details><summary>show</summary>
<p>

macOS. It costs 10 times (in terms of minutes of compute) the price of a Linux minute.

</p>
</details>

### What are the different types of support for Enterprise Support?

<details><summary>show</summary>
<p>

- GitHub Enterprise Support (Included with Enterprise Cloud and Enterprise Server)
- GitHub Enterprise Premium support
- GitHub Enterprise Premium Plus support

</p>
</details>

### What kind of info can you find using the Audit Log API?

<details><summary>show</summary>
<p>

- Accesses your organization or repository settings.
- Changes permissions.
- Adds or removes users in an organization, repository, or team.
- Promotes users to admin.
- Changes permissions of a GitHub App.

</p>
</details>

### Does the support cover account, server, and security issues?

<details><summary>show</summary>
<p>

No, it covers Account, Security, and Abuse issues.

</p>
</details>

### Does GitHub Enterprise Server contain the GitHub Actions feature?

<details><summary>show</summary>
<p>

Yes. It is disabled by default but it's there and it contains already some built-in actions created by GitHub. It does NOT require access to Internet to work because you can sync/download the Actions locally.

</p>
</details>

### Does GitHub Enterprise Server contain the GitHub Packages feature?

<details><summary>show</summary>
<p>

Yes.

</p>
</details>

## Manage access and permissions based on membership

### What are the two roles available at the team level?

<details><summary>show</summary>
<p>

- member
- maintainer

</p>
</details>

### What are the three roles available at the organization level?

<details><summary>show</summary>
<p>

- owner
- member
- billing manager

</p>
</details>


### Which role access should you give to a contributor with full control on the repo except access to sensitive or destructive actions?

<details><summary>show</summary>
<p>

**maintainer** because **admin** role would for instance allow to delete a repo.

</p>
</details>

### What is the appropriate repository permission level for contributors who will actively push changes to your repository?

<details><summary>show</summary>
<p>

**write**

</p>
</details>

### By default, can all users of an organization see all repositories?

<details><summary>show</summary>
<p>

Yes if the "Read" access is defined as default role in "base permissions" in the organization's settings.

</p>
</details>

### Which role allows a person to manage issues of a repository without any write rights?

<details><summary>show</summary>
<p>

**triage**

</p>
</details>

### What is a deploy key?

<details><summary>show</summary>
<p>

You can launch projects from a repository on GitHub.com to your server by using a deploy key, which is an SSH key that grants access to a single repository. GitHub attaches the public part of the key directly to your repository instead of a personal account, and the private part of the key remains on your server.

</p>
</details>

## Enable secure software development and ensure compliance

### How can you exclude sensitive files from your repository?

<details><summary>show</summary>
<p>

One technique to help avoid the majority of this risk is to build and maintain **.gitignore** files

</p>
</details>

### Once sensitive data has been committed, can you erase the history to keep the data secret again?

<details><summary>show</summary>
<p>

**No**. You can overwrite a commit but you must consider the data insecure once it has been committed. If it's a secret/password, then you must renew it.

</p>
</details>

### What is the starting point to enforce certain workflows like passing security checks?

<details><summary>show</summary>
<p>

You should use [branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule).

</p>
</details>

### How can you automatically assign specific persons as reviewers when a part of the code is modified?

<details><summary>show</summary>
<p>

You should use [CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners#codeowners-syntax) files.

</p>
</details>

### What is the simplest way to prevent the creation of public repositories?

<details><summary>show</summary>
<p>

At the organization level, in "Member privileges" settings, disallow the creation of public repositories.

</p>
</details>

### If you plan to communicate about your security policy, like disclosing vulnerabilities, where should you store your policy publicly?

<details><summary>show</summary>
<p>

In the root of your repository in a file named SECURITY.md.

</p>
</details>


### Using branch protection rules, which setting prevents merge commits?

<details><summary>show</summary>
<p>

**Require linear history** ([see documentation](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches#require-linear-history))

</p>
</details>

### In which part of your repository can you find the dependency graph listing all the packages your repo depends on?

<details><summary>show</summary>
<p>

In the **Insights** tab and then **Dependency graph**.
</p>
</details>


### Which feature of GitHub scans your repo and alerts you in case of detected vulnerabilities in your dependencies?

<details><summary>show</summary>
<p>

**GitHub Security Advisories**.
</p>
</details>


### Which feature of GitHub scans your repo and alerts you in case of detected vulnerabilities and automatically creates a pull request to fix it?

<details><summary>show</summary>
<p>

**Dependabot**.
</p>
</details>

### What is the feature which helps to prevent committing a secret?

<details><summary>show</summary>
<p>

If you want to act **before** a commit, you must use a pre-commit hook which allows you to scan the code before the commit.

</p>
</details>

### Which tools can be used to tamper with Git history and erase sensitive data?

<details><summary>show</summary>
<p>

**git filter-repo** & **BFG Repo-Cleaner**

</p>
</details>

### Which two pieces of information should be included in a security advisory?

<details><summary>show</summary>
<p>

**Product affected** and **severity**

</p>
</details>

### You have a workflow secret named MY_SECRET. What is the format to call it from the workflow?

<details><summary>show</summary>
<p>

```yaml
steps:
  - name: Hello world action
    with: # Set the secret as an input
      super_secret: ${{ secrets.MY_SECRET }}
```

</p>
</details>

## Manage GitHub Actions

### Which two files are mandatory when creating a workflow template?

<details><summary>show</summary>
<p>

- a workflow file with a yml extension (**my-workflow**.yml)
- a properties file with ".properties.json" extension (**my-workflow**.properties.json)

Both files must have the same name.

</p>
</details>

### Which placeholder keyword allows you to inject the current default branch in a workflow template?

<details><summary>show</summary>
<p>

**$default-branch**

```yaml
on:
  push:
    branches: [ $default-branch ]
```

</p>
</details>

### Can you prevent users from using Actions from the marketplace?

<details><summary>show</summary>
<p>

Yes, using Policies and restricting to local actions only.

</p>
</details>

### Can you allow users to only use actions created by GitHub or verified creators?

<details><summary>show</summary>
<p>

Yes, using Policies and restricting to specific actions (menu "Allow select actions").

</p>
</details>

### Are the Actions created by GitHub automatically present in GitHub Enterprise Server?

<details><summary>show</summary>
<p>

Yes, but they may not be the last version of them.

</p>
</details>

### Which feature allows you to provide pre-made templates to users when they want to create a workflow?

<details><summary>show</summary>
<p>

It's called a **workflow template**.

</p>
</details>

### What are the default labels applied to a self-hosted agent?

<details><summary>show</summary>
<p>

- *self-hosted*
- the os: *linux*, *windows*, or *macOS*
- the CPU architecture: *x64* , *ARM*, or *ARM64*

</p>
</details>

### How do you enforce your workflow running on a specific self-hosted agent running on Linux with ARM?

<details><summary>show</summary>
<p>

```yaml
runs-on: [self-hosted, linux, ARM64]
```

</p>
</details>

### In which folder of a self-hosted agent can you find logs to debug the behavior of the runner?

<details><summary>show</summary>
<p>

In the *_diag* folder.

</p>
</details>

## Manage GitHub Packages

### Can you upload container images in GitHub Packages?

<details><summary>show</summary>
<p>

Yes.

</p>
</details>

### What is the Docker command to publish a container image on GitHub Packages?

<details><summary>show</summary>
<p>

```bash
docker push ghcr.io/OWNER/IMAGE_NAME:latest
```

</p>
</details>

### What are the (programming) package managers supported by GitHub Packages?

<details><summary>show</summary>
<p>

- npm, a Node.js package manager
- NuGet, the .NET package manager
- RubyGems
- Maven and Gradle, two package managers for Java

</p>
</details>

### In which scenarios should you NOT use GitHub Packages?

- [ ] When I want to share code between methods of my application.
- [ ] When I want to share container images among developers of your team.
- [ ] When I want to publish a small code library as an open-source project.

<details><summary>show</summary>
<p>

**When I want to share code between methods of my application**

</p>
</details>

### What is Enterprise Managed Users (EMU)?

<details><summary>show</summary>
<p>

Enterprise Managed Users is a deployment option where user accounts are provisioned and managed by the enterprise through an identity provider (IdP). With EMU:
- Users cannot create their own accounts
- All authentication goes through the enterprise IdP
- Users can only contribute to repositories within the enterprise
- Provides complete lifecycle management of user accounts

</p>
</details>

### What is the difference between organization secrets and repository secrets?

<details><summary>show</summary>
<p>

- **Organization secrets**: Shared across multiple repositories in an organization, can be scoped to specific repositories or all repositories
- **Repository secrets**: Only accessible within a single repository

Organization secrets are useful for credentials that need to be shared, like cloud provider access keys.

</p>
</details>

### How do you configure IP allow lists for an organization?

<details><summary>show</summary>
<p>

IP allow lists restrict access to organization resources to specific IP addresses or CIDR ranges:

1. Go to Organization Settings → Security → IP allow list
2. Add allowed IP addresses or CIDR ranges
3. Enable the IP allow list

This applies to web, API, and Git access.

</p>
</details>

### What is a runner group?

<details><summary>show</summary>
<p>

Runner groups are collections of self-hosted runners that can be shared across an organization. They allow you to:
- Control which repositories can use specific runners
- Organize runners by purpose or environment
- Set access policies at the group level

By default, all runners are added to a default group.

</p>
</details>

### What are the different types of GitHub Enterprise licenses?

<details><summary>show</summary>
<p>

- **GitHub Enterprise Cloud**: Hosted by GitHub, includes advanced security features, cloud-based
- **GitHub Enterprise Server**: Self-hosted on your own infrastructure, runs behind your firewall

Both can be combined for maximum flexibility.

</p>
</details>

### How do you transfer a repository between organizations?

<details><summary>show</summary>
<p>

To transfer a repository:
1. Go to Repository Settings → General
2. Scroll to "Danger Zone"
3. Click "Transfer"
4. Enter the new owner (organization or user)
5. Confirm the transfer

The repository must not have any outstanding sponsorship or Actions billing.

</p>
</details>

### What happens to forks when a repository is deleted?

<details><summary>show</summary>
<p>

When a public repository with forks is deleted:
- One of the forks becomes the new root repository
- All other forks remain linked to this new root

When a private repository with forks is deleted:
- All forks are deleted if the repository network is not preserved

</p>
</details>

### What is the purpose of a default community health file?

<details><summary>show</summary>
<p>

Default community health files stored in a `.github` repository apply to all repositories in the organization that don't have their own versions. These include:
- CODE_OF_CONDUCT.md
- CONTRIBUTING.md
- SECURITY.md
- SUPPORT.md
- Issue and PR templates
- FUNDING.yml

</p>
</details>

### How do you enforce SAML single sign-on for an organization?

<details><summary>show</summary>
<p>

To enforce SAML SSO:
1. Navigate to Organization Settings → Security
2. Enable SAML single sign-on
3. Configure your identity provider settings
4. Test the configuration
5. Click "Require SAML SSO authentication"

After enforcement, members must authenticate through the IdP to access resources.

</p>
</details>

### What is the difference between archiving and deleting a repository?

<details><summary>show</summary>
<p>

**Archiving:**
- Repository becomes read-only
- All content is preserved
- Issues, PRs, and discussions are locked
- Can be unarchived later
- Useful for projects no longer actively maintained

**Deleting:**
- Permanently removes the repository
- Cannot be undone after grace period
- Removes all issues, PRs, and history

</p>
</details>
