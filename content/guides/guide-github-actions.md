# GitHub Actions

## Prerequisites

- Basic understanding of CI/CD concepts
- Familiarity with YAML syntax
- Basic knowledge of command-line interfaces
- Understanding of Git and GitHub fundamentals

## Skills measured

- Author and maintain workflows (40%) - Approx 29 Questions
- Consume workflows (20%) - Approx 14 Questions
- Author and maintain actions (25%) - Approx 18 Questions
- Manage GitHub Actions for the enterprise (15%) - Approx 11 Questions

## Key Concepts to Master

### Workflow Fundamentals
- Workflow syntax and structure
- Events and triggers (push, pull_request, schedule, workflow_dispatch)
- Jobs, steps, and actions
- Runners (GitHub-hosted vs self-hosted)
- Workflow permissions and security

### Expressions and Contexts
- GitHub contexts (github, env, job, steps, runner, secrets)
- Expressions syntax (${{ }})
- Status check functions (success(), failure(), always(), cancelled())
- Conditional execution (if statements)

### Variables and Secrets
- Environment variables (env context)
- Repository secrets and organization secrets
- Configuration variables
- GITHUB_TOKEN and permissions

### Reusability
- Composite actions
- Reusable workflows
- Workflow templates
- Action versioning strategies

### Advanced Features
- Matrix strategies for parallel jobs
- Concurrency control
- Caching and artifacts
- Service containers
- Environments and deployment protection

## Learning path

I recommend the book "GitHub Actions: a practical guide" (available in [english](https://www.amazon.com/GitHub-Actions-practical-Louis-Guillaume-MORAND-ebook/dp/B09D3Z3Y48) and in [french](https://www.amazon.fr/GitHub-Actions-pratique-Louis-Guillaume-MORAND/dp/2957832941/)). 
As an alternative, there is a [Microsoft Learn path](https://docs.microsoft.com/en-us/users/githubtraining/collections/n5p4a5z7keznp5) but it does **not** cover everything such as authoring custom GitHub Actions.

In addition, I recommend [this module](https://docs.microsoft.com/en-us/learn/modules/manage-github-actions-enterprise/introduction) which is not in the learning path but present in the exam.

### Additional Resources

- [GitHub Actions documentation](https://docs.github.com/en/actions) - Official comprehensive documentation
- [GitHub Actions Marketplace](https://github.com/marketplace?type=actions) - Browse and discover actions
- [GitHub Skills - GitHub Actions courses](https://skills.github.com/) - Hands-on interactive learning
- [Awesome Actions](https://github.com/sdras/awesome-actions) - Curated list of GitHub Actions
- [GitHub Actions Changelog](https://github.blog/changelog/label/actions/) - Latest updates and features

### Tips for the Exam

1. **Practice creating workflows** - Hands-on experience is essential
2. **Understand triggers deeply** - Know the differences between push, pull_request, workflow_dispatch, etc.
3. **Master the matrix strategy** - Understand how to create combinations and exclusions
4. **Know your contexts** - github, env, secrets, jobs, steps, runner contexts
5. **Understand action types** - Docker, JavaScript, and Composite actions

## Test exam

When you are ready, you can test your skills with the [test exam](../exams/exam-github-actions.md).
