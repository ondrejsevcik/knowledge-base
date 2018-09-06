# Finds my TODOs in git codebase

```sh
git grep -il TODO | xargs -n1 git blame -M  -f -e | grep -i TODO | grep $(git config user.email)
```
