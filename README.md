# Getting Started with Hugo
1. Install hugo
```brew install hugo```
2. Generate a site
```hugo new site INSERT_SITE_NAME```
3. Change into site directory
```cd INSERT_SITE_NAME```
4. Choose a theme and add it as a submodule e.g.
```git submodule add https://github.com/apvarun/blist-hugo-theme.git themes/blist```
5. Follow instructions for site theme
6. Serve the content locally
```hugo server```
7. Create a new repo with name that will be your github pages url for hosting e.g. moneywisesidehustler.github.io
8. Create a new post
```hugo new blog/intro.md```
9. Remove "draft: true" line as it will stop page being published
10. Add that repo as a submodule, you may need to delete the public folder first
```git submodule add -b main https://github.com/USER_HERE/REPO_NAME.git public```
11. Generate the static content using the command
```hugo -t THEME_NAME```
12. Change directory into the public directory and commit and push the static pages. This will publish the content to you github pages URL.
13. Repeat steps 8-12 as required to add additional content.