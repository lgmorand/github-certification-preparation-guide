# GitHub Entreprise

## Skills measured

- Support GitHub Enterprise for users and key stakeholders
- Manage user identities and GitHub authentication
- Describe how GitHub is deployed, distributed, and licensed
- Manage access and permissions based on membership
- Enable secure software development and ensure compliance
- Manage GitHub Actions
- Manage GitHub Packages

### What role is required to edit a team ?

<details><summary>show</summary>
<p>

**Maintainer** or **admin**

</p>
</details>

### Can be GitHub synchronized with an identity provider ?

<details><summary>show</summary>
<p>

Yes, for instance, Azure Active Directory but other like ADFS, Okta, OneLogin, etc

</p>
</details>

### Can you have nested teams in GitHub ?

<details><summary>show</summary>
<p>

Yes and it is a general pratice [to use them to reflect](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams#nested-teams) the current enterprise internal's organization.

</p>
</details>

### What are the different methods to authenticate against GitHub ?

<details><summary>show</summary>
<p>

- username/password
- PAT (Personal Access Token)
- SSH keys
- Deploy keys

</p>
</details>

### Which role access should you give to a contributor with full control on the repo except access to sensitive or destructive actions  ?

<details><summary>show</summary>
<p>

**maintainer** because **admin** role would for instance allow to delete a repo

</p>
</details>

## What is the appropriate repository permission level for contributors who will actively push changes to your repository

<details><summary>show</summary>
<p>

**write**

</p>
</details>

### What are the two roles available at team level  ?

<details><summary>show</summary>
<p>

- member
- maintainer

</p>
</details>

### What are the three roles available at organization level  ?

<details><summary>show</summary>
<p>

- owner
- member
- billing manager

</p>
</details>


### By default, can all users of an organization see all repositories ?

<details><summary>show</summary>
<p>

Yes if the "Read" access is defined as default role in "base permissions" in the organization's settings

</p>
</details>

### What is the simplest way to prevent the creation of public repository  ?

<details><summary>show</summary>
<p>

At the organization level, in "Member privileges" settings, disallow the creation of public repositories.

</p>
</details>


### Can an enterprise contain several organizations  ?

<details><summary>show</summary>
<p>

yes.

</p>
</details>


### Are the hosted agents totally free ?

<details><summary>show</summary>
<p>

Yes for public repositories. For private repositories, you have free minutes of usage offered per month

</p>
</details>

### You plan on using GitHub Actions to build, test, and deliver your cross-platform code. Which of the following platforms will be the most expensive to use?

<details><summary>show</summary>
<p>

macOS. It cost 10 times (in terms of minute of compute) the price of a linux minute

</p>
</details>

### If you plan to communicate about your security policy, like disclosing vulnerabilities, where should you store your policy publicly ?

<details><summary>show</summary>
<p>

In the root of your repository in a file named SECURITY.md.

</p>
</details>

### How can you exclude sensitive files from your repository ?

<details><summary>show</summary>
<p>

One technique to help avoid the majority of this risk is to build and maintain **.gitignore** files

</p>
</details>


### Once a sensitive data has been commited, can you erase the history to keep the data secret again ?

<details><summary>show</summary>
<p>

**No**. You can overwrite a commit but you must consider the data unsecure once it has been commited. If it's a secret/password, then you must renew it.

</p>
</details>

### What is the starting point to enforce certain workflows like passing security checks ?

<details><summary>show</summary>
<p>

You should use [branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule).

</p>
</details>

### How can you automatically assign specific persons as reviewers when a part of the code is modified ?

<details><summary>show</summary>
<p>

You should use [CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners#codeowners-syntax) files.

</p>
</details>

### In which part of your repository can you find the dependency graph listing all the packages your repo depends on ?

<details><summary>show</summary>
<p>

In the **Insights** tab and then **Dependency graph**.
</p>
</details>


### Which feature of GitHub scan your repo and alerts you in case of detected vulnerabilities in your dependencies ?

<details><summary>show</summary>
<p>

**GitHub Security Advisories**.
</p>
</details>


### Which feature of GitHub scan your repo and alerts you in case of detected vulnerabilities and automatically create a pull request to fix it ?

<details><summary>show</summary>
<p>

**Dependabot**.
</p>
</details>

### What is the feature which help to prevent to commit a secret ?

<details><summary>show</summary>
<p>

If you want to act **before** a commit, you must use pre-commit hook which allow to scan the code before the commit.

</p>
</details

### Which tools can be used to tamper Git history and erase sensitive data ?

<details><summary>show</summary>
<p>

**git filter-repo** & **BFG Repo-Cleaner**

</p>
</details

### Which tools can be used to tamper Git history and erase sensitive data ?

<details><summary>show</summary>
<p>

**git filter-repo** & **BFG Repo-Cleaner**

</p>
</details


### Which two pieces of information should be included in a security advisory

<p>

**Product affected** and **severity**

</p>
</details