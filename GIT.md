# Git이란,
  - git: help tracking file changes(version control)
  - git view file as binary form(git can track any file format)
  - commit
    : capture its point of changes
# GitHub이란,
  - github: upload file and its changes detail
  - respository
    : folder that has code changes and its history

# GitHub for beginner
  - How to create respository:
    - `new` button in github
	- name respository at `respository name`
	  - no spaces, lowercase
	- description optional
	- make your code in public
  - Github Desktop
    - beginner-friendly GUI git manager
	- Connect respository to local path
  - How to make commit:
    - make progress of your project
	- checkbox your file change at GitHub Desktop
	- name commit's title
	- press button `Commit to master`
	- publish branch to github
  - create `.gitignore`
    - exclude irrelevant files and folders from project
	- `[FILENAME].[EXTENSION]`
	- `*.[EXTENSION]`
	- `/[FOLDERNAME]`
  - Git branch
    - branch is like a parallel version of your project
	- when you want to experiment feature, leave main branch as stable one and test it with new branch
	- when new branch is successful, commit it and you can merge the orginal one
	  - use `Merge into Current Branch` at Main Branch
	- you can switch current branch with GitHub Desktop

# 7.1 Publish GitHub Pages
  - GitHub Pages: GitHub provide publish(hosting) of static website
  - create `gh-pages` branch
    - `git checkout -b gh-pages`
	- `git push origin gh-pages`
  - view it on `[USERNAME].github.io/[PROJECTNAME]`
  - when update gh-pages
    - don't edit gh-pages or it will break
	  - only edit from main branch
    - `update from main`
	- `push to origin`
  * static website: website that consist of only HTML / CSS / JavaScript

# update gh-page branch with CLI
  - `git checkout gh-pages`
  - `git rebase master`
  - `git push origin gh-pages`
  - `git checkout master`
# Start Project
  - Git Setup
  - `README.md` 
  
  * md: markdown file; document that has format
  * md syntax
    - #