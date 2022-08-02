# GitHub Actions

> These are NOT real questions from the exam but quite close enough to help you to prepare it and obtain the certification

## Skills measured

- [Author and maintain workflows](#author-and-maintain-actions) (40% of the exam)
- [Consume workflows](#consume-workflows) (20% of the exam)
- [Author and maintain actions](#manage-github-actions-for-the-enterprise) (25% of the exam)
- [Manage GitHub Actions for the enterprise](#manage-github-actions-for-the-enterprise) (15% of the exam)

## Author and maintain workflows

### How to trigger a workflow when a commit is done on the main branch ?

<details><summary>show</summary>
<p>

```yaml
on:
  push:
    branches:
      - main
```

</p>
</details>

### How to trigger a workflow when a pull request is done on the main branch ?

<details><summary>show</summary>
<p>

```yaml
on:
  pull_request:
    branches:
      - main
```

</p>
</details>

### What is the keyword to ensure a job must run after another successful job ?

<details><summary>show</summary>
<p>

**needs**

```yaml
jobs:
  job1:
  job2:
    needs: job1
  job3:
    needs: [job1, job2]
```
</p>
</details>






###  In which folder must be placed your workflows's YAML files?

<details><summary>show</summary>
<p>

```
.github/workflows
```

</p>
</details>

### Suppose you have created a bug fix on a new branch and want it to become part of the next production build generated from the main branch. What should you do next? ?

<details><summary>show</summary>
<p>

Create a pull request to merge your new branch into the main branch.

</p>
</details>

### What is the keyword to specify the operating system on which the job will be executed ?

<details><summary>show</summary>
<p>

**runs-on**

```yaml
jobs:
  print-username:
    runs-on: ubuntu-latest
    steps:
```

</p>
</details>





## Consume workflows

## Author and maintain actions


## Manage GitHub Actions for the enterprise




### What are the three different ways to call a version of an Action

<details><summary>show</summary>
<p>

- the branch name
- the version (semver)
- the commit hash

```yaml
steps:
  - uses: github/my-action@v1
  - uses: github/my-action@main
  - uses: github/my-action@734713bc047d87bf7eac9674765ae793478c50d3
```

</p>
</details>

### What are the two "secure" ways to call a specific version of an Action

<details><summary>show</summary>
<p>

- the version (semver)
- the commit hash

```yaml
steps:
  - uses: github/my-action@v1
  - uses: github/my-action@734713bc047d87bf7eac9674765ae793478c50d3
```

The branch name is not secure as it can change at anytime. The version (using semver) is most secure IF the developer never overwrite a previous version
</p>
</details>




### Which variable contains the name of the repository and the name of the owner ?

<details><summary>show</summary>
<p>

**GITHUB_REPOSITORY**

</p>
</details>

### Which variable contains the name of the user who triggered the workflow ?

<details><summary>show</summary>
<p>

**GITHUB_ACTOR**

</p>
</details>

### Which variable contains the name of the branch or tag which triggered the current workflow ?

<details><summary>show</summary>
<p>

**GITHUB_REF_NAME**

/!\ GITHUB_REF will contains the full name (*refs/heads/<branch_name>*)

</p>
</details>
### Do the jobs of a workflow run on the same machine ?

<details><summary>show</summary>
<p>

```yaml

```

</p>
</details>

###  How to call a variable which has been defined as a secret ?

<details><summary>show</summary>
<p>

```yaml

```

</p>
</details>

### How to create a manual approbal step in a workflow ?

<details><summary>show</summary>
<p>

```yaml

```

</p>
</details>



### Which operating systems are supported to run GitHub Actions on hosted agents?

<details><summary>show</summary>
<p>

- Linux (ubuntu)
- Windows (windows server)
- Mac OS
  
</p>
</details>


### Which trigger allows to start a workflow manually ?

<details><summary>show</summary>
<p>

**workflow_dispatch**
  
</p>
</details>


### How many combinations are created with the following matrix  ?

```yaml
jobs:
  example_matrix:
    strategy:
      matrix:
        version: [10, 12, 14]
        os: [ubuntu-latest, windows-latest]
```

<details><summary>show</summary>
<p>

6 combinations
  
</p>
</details>