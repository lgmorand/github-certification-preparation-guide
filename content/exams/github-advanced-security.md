# GitHub Advanced Security

> These are NOT real questions from the exam but quite close enough to help you to prepare it and obtain the certification

## Skills measured

- [Describe the GitHub Advanced Security features and functionality](#describe-github-advanced-security-best-practices-results-and-how-to-take-corrective-measures)
- [Configure and use secret scanning](#configure-and-use-code-scanning)
- [Configure and use dependency management](#configure-and-use-dependency-management)
- [Configure and use code scanning](#configure-and-use-code-scanning)
- [Use code scanning with CodeQL](#use-code-scanning-with-codeql)
- [Describe GitHub Advanced Security best practices, results, and how to take corrective measures](#describe-github-advanced-security-best-practices-results-and-how-to-take-corrective-measures)
- [Configure GitHub Advanced Security tools in GitHub Enterprise](#configure-github-advanced-security-tools-in-github-enterprise)

## Describe the GitHub Advanced Security features and functionality

### GitHub Advanced Security focuses on protecting your organization in three primary areas. Which are?

<details><summary>show</summary>
<p>

- Supply chain
- Code
- Environments

</p>
</details>

### Which area of focus does GitHub dependency management belong to?

- Code scanning
- Policies
- Supply chain

<details><summary>show</summary>
<p>

Supply chain

</p>
</details>

### What is the name of the feature which provides Code Scanning on GitHub?

<details><summary>show</summary>
<p>

CodeQL

</p>
</details>

### What does the term 'shifting left' mean?

<details><summary>show</summary>
<p>

Incorporating security principles early in the software development lifecycle

</p>
</details>

### What is the features which provides a safe space for code maintainers to discuss how to best address errors and vulnerabilities found in the codebase ?

<details><summary>show</summary>
<p>

security advisories
</p>
</details>

### What are the main security features availables with GitHub Advanced Security ?

<details><summary>show</summary>
<p>

- Dependabot
- Code scanning (CodeQL or 3rd party)
- Secret scanning

</p>
</details>

## Configure and use secret scanning

### Can secret scanning detect a specific connection string for a Cloud provider such as Azure or AWS ?

<details><summary>show</summary>
<p>

Yes. A lot of [providers formats](https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns) can be detected within the source code.

</p>
</details>

### Which branch(s) is (are) scanned to detect the secrets ?

- the main/master branch
- the default branch
- the active branch (last 30 days)
- all the branchs

<details><summary>show</summary>
<p>

ALL the branchs

</p>
</details>

### How many days in Git history are scanned ?

<details><summary>show</summary>
<p>

ALL history is scanned.

</p>
</details>

### In which tab of the repository can you find the detected secrets  ?

<details><summary>show</summary>
<p>

In the **Security** > **Secret scanning** screen.

</p>
</details>

### Can you add custom patterns to detect specific secrets ?

<details><summary>show</summary>
<p>

Yes, you can add up to 100 custom patterns.

</p>
</details>

### Can you prevent a user to commit a secret ?

<details><summary>show</summary>
<p>

No, or you need a local software to scan pre-commit.

</p>
</details>

### Can you prevent to push a commit which contain a secret ?

<details><summary>show</summary>
<p>

Yes, you can enable [**push protection**](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/protecting-pushes-with-secret-scanning) which scans the content of the commit before allowing it on the server.

</p>
</details>

### Can a user bypass push protection?

<details><summary>show</summary>
<p>

Yes, but then it generates an alert in the Security tab, a bypass even is added to the audit log and an email is sent to org owners, security managers and repo administrators.

</p>
</details>

### Can secret scanning rotate your detected secret automatically for you ?

<details><summary>show</summary>
<p>

No but in some cases, GitHub also notifies the service provider who issued the secret. The service provider can then take any appropriate action like revoking the secret, issuing a new secret or reaching out to you directly depending on the associated risks to you or them.

</p>
</details>

### Can you have secret scanning for free ?

<details><summary>show</summary>
<p>

Yes, it is enabled by default on all public repositories. It **cannot be configured or turned off**. Secret scanning **must be enabled manually** on private repositories but it then a paid option.

</p>
</details>

### What is the best way to enable secrets scanning at scale ?

<details><summary>show</summary>
<p>

You can enable it at organization level to enable it by default on all private repositories.

Follow the steps below to enable secret scanning for an organization:

- In your organization, navigate to Settings > Security & analysis.
- Under Configure security and analysis features, click the Enable all button next to GitHub Advanced Security.
- Review the impact of enabling Advanced Security on all repositories and click Enable all.
- Click the Enable all button next to Secret scanning.
- Optionally enable the feature by default for new repositories in your organization, and click Enable for eligible repositories.


</p>
</details>

### What is the name of the file to list paths/files to exclude from secret scanning ?

<details><summary>show</summary>
<p>

The file **.github/secret_scanning.yml** and then using the keyword **paths-ignore**

```yaml
paths-ignore:
  - "foo/bar/*.js"
```

> If there are more than 1,000 entries in paths-ignore, secret scanning will only exclude the first 1,000 directories from scans.
  If secret_scanning.yml is larger than 1 MB, secret scanning will ignore the entire file.

</p>
</details>




## Configure and use dependency management
## Configure and use code scanning
## Use code scanning with CodeQL
## Describe GitHub Advanced Security best practices, results, and how to take corrective measures

## Configure GitHub Advanced Security tools in GitHub Enterprise

