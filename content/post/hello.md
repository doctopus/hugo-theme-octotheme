---
title: "Hello"
date: 2022-10-09T23:31:41+05:30
draft: false
---

### Install Hugo
[https://gohugo.io/getting-started/quick-start/](https://gohugo.io/getting-started/quick-start/)

```brew install hugo```

In github create two repos blog and username.github.io   
Clone blog at your local computer

```go
cd blog  
hugo new site doctopus
```

Creates a doctopus folder inside blog/  
Doctopus folder will have the boilerplate folders
Since the blog folder is cloned git is already init in it.

Install the theme of choice as a submodule in the themes folder

`git submodule add https://github.com/xxx/hugo-theme.git themes/hugo-theme`

Notice that this folder was added as a submodule so it can not be deleted. If it needs to be removed it needs to be removed using following process.    

### Removing Submodule in a Main Git Module
If a submodule is wrongly added. Just deleting it will not remove it, instead do the following

```go
git submodule deinit <path_to_submodule>

git rm <path_to_submodule>

git commit-m "Removed submodule "

rm -rf .git/modules/<path_to_submodule>`