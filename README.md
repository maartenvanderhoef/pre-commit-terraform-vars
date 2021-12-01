# pre-commit-shfmt hook

### Copy of git://github.com/pecigonzalo/pre-commit-terraform-vars with added logic for unused locals


Single [pre-commit](http://pre-commit.com/) hook which runs **[terraform_unused_vars](https://github.com/ContainerLabs/terraform-unused-vars)** on the terraform project.


To skip a local from failing use:
```
  #terraform_unused_vars:skip=local.the_local_to_be_skipped
```

An example `.pre-commit-config.yaml`:

```yaml
-   repo: git://github.com/maartenvanderhoef/pre-commit-terraform-vars
    rev: v2.0.0
    hooks:
      -   id: terraform-vars
```
