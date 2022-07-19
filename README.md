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

# Adding a custom domain
1. Navigate to your github pages repo - this is the repo that hosts your static content
2. Go to Settings and then Pages
3. Add your custom domain (including subdomain and click save). This will add a CNAME file to your repo.
4. Go to your config.toml and update your baseURL or your theme will die. Include HTTPS.
5. Go to your domain name provider and add a CNAME record, name being the subdomain and data being your github pages url e.g. moneywisesidehustler.github.io.
6. Use the command ```hugo -t blist``` to build your static site
7. Push the changes in your blog repo and public folder to GitHub
8. Wait for HTTPS certificate to be provided then enforce HTTPS

# Adding Google Ads
1. Login to adsense and get the adsense script provided for your site
2. Go to themes/THEME_NAME/partials and add a google folder. To that add a file ads.html with your adsense script
3. Go to where the metadata is being added to your site in the header e.g. head.html in the case of blist and add the following line, which will add the script to your file:
```{{ partial "google/ads" . }}```
4. Use the command ```hugo -t blist``` to build your static site
5. Push the changes in your blog repo and public folder to GitHub
6. Request your site to be verified