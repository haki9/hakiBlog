---
date: "2019-03-20"
title: "Home"
---

Welcome to **Haki Blog**


## Step 1. Install Hugo

MAC OS

{{< cmd >}}
brew install hugo
{{< /cmd >}}


## Step 2. Create A Project

{{< cmd >}}
hugo new site myblog
{{< /cmd >}}

## Step 3. Add Themes

{{< cmd >}}
cd myblog
git init
git submodule add https://github.com/zwbetz-gh/cupper-hugo-theme.git themes/cupper-hugo-theme
cp theme/cupper-hugo-theme/exampleSite/config.toml config.toml
{{< /cmd >}}

Copy folders and files in **themes/cupper-hugo-theme/exampleSite/content** to **root content**

## Step 4. Run

{{< cmd >}}
hugo server
{{< /cmd >}}


## Step 4. Upload to Github Pages

Create two repositories: **hugo-blog** and **blog**

In myblog path
{{< cmd >}}
git remote add origin https://github.com/hugo-blog
vim .gitignore
{{< /cmd >}}

Insert *public/* to .gitignore file

{{< cmd >}}
git add .
git commit -m "initial commit"
git push origin master
cd ..
git clone git remote add origin https://github.com/blog
cd myblog
hugo -d ../blog
cd ..
cd blog
git add .
git commit -m "initial commit"
git push origin master
{{< /cmd >}}

{{% note %}}
Change **baseURL** in config.toml when deploy on server
{{% /note %}}


## Step 5. Have fun

The best way to learn something is to play with it.
