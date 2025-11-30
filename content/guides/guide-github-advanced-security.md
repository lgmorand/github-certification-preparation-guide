# GitHub Advanced Security

## Prerequisites

- Familiarity with a GitHub Enterprise Cloud or Enterprise Server account with GitHub Advanced Security
- Working knowledge of GitHub Actions and workflows
- Basic understanding of security concepts and application security

## Skills measured

- Describe the GitHub Advanced Security features and functionality (10%) - Approx 7 Questions
- Configure and use secret scanning (10%) - Approx 7 Questions
- Configure and use dependency management (15%) - Approx 10 Questions
- Configure and use code scanning (15%) - Approx 10 Questions
- Use code scanning with CodeQL (20%) - Approx 14 Questions
- Describe GitHub Advanced Security best practices, results, and how to take corrective measures (18%) - Approx 12 Questions
- Configure GitHub Advanced Security tools in GitHub Enterprise (12%) - Approx 8 Questions

## Key Concepts to Master

### Security Overview
- Security Dashboard navigation
- Risk and coverage views
- Alert prioritization
- Security trends and metrics

### Secret Scanning
- Supported secret types
- Push protection
- Custom patterns
- Alert management
- Partner program integration

### Dependency Management
- Dependency graph
- Dependabot alerts
- Dependabot security updates
- Dependabot version updates
- Advisory database

### Code Scanning
- CodeQL analysis
- SARIF file format
- Third-party tool integration
- Query suites and custom queries
- Alert triaging

### CodeQL
- Query language basics
- Built-in queries
- Custom query creation
- CodeQL CLI
- Analysis configuration

### Enterprise Configuration
- Enabling GHAS at scale
- Organization policies
- Licensing and billing
- API and webhooks

## Learning path

I recommend the [Microsoft Learn path](https://docs.microsoft.com/en-us/users/githubtraining/collections/rqymc6yw8q5rey).

### Additional Resources

- [GitHub Advanced Security documentation](https://docs.github.com/en/code-security) - Official documentation
- [CodeQL documentation](https://codeql.github.com/docs/) - Query language reference
- [GitHub Advisory Database](https://github.com/advisories) - Security advisories
- [Secret scanning patterns](https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns) - Supported patterns
- [SARIF specification](https://sarifweb.azurewebsites.net/) - SARIF format reference

### Tips for the Exam

1. **Understand the three pillars**: Secret scanning, Dependency review, Code scanning
2. **Know CodeQL supported languages**: C/C++, C#, Go, Java, JavaScript/TypeScript, Python, Ruby
3. **Master push protection**: When it blocks, bypass options, and audit logs
4. **Understand Dependabot configuration**: dependabot.yml file structure
5. **Learn alert states**: Open, dismissed, fixed, and their implications

## Test exam

When you are ready, you can test your skills with the [test exam](../exams/exam-github-advanced-security.md).
