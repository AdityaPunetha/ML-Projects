# ML-Projects

Compiling multiple ML Projects repos into single one
---
If you want to merge project-a into project-b:

```
cd path/to/project-b
git remote add project-a /path/to/project-a
git fetch project-a --tags
git merge --allow-unrelated-histories project-a/master # or whichever branch you want to merge
git remote remove project-a
Taken from: git merge different repositories?
```

In case you want to put project-a into a subdirectory, you can use git-filter-repo (filter-branch is discouraged). Run the following commands before the commands above:

```
cd path/to/project-a
git filter-repo --to-subdirectory-filter project-a
```

https://stackoverflow.com/questions/1425892/how-do-you-merge-two-git-repositories
