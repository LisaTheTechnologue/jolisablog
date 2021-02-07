---
layout: post
title:  "Table of Contents with Jekyll"
date:   2020-02-03 20:00:00 -0500
categories: [it,Git, Github pages]
tags: [IT, git, gh-pages]
---

1. Installation         
Go to RubyInstaller and download installer.              
`rdik install` will be run next. Make sure it run successfully all.            
Run `gem install jekyll bundler` will install jekyll.                 

Check if successfully install:                
```
ruby -v                
gem -v                  
jekyll -v                         
```

2. Create local Jekyll's project folder.                  
```
jekyll new project_name && cd project_name
```
This will create all basic files such as Gem, _config.yml, etc

3. Run locally                       
```
bundle                     
bundle exec jekyll s
```
`bundle` is used for install necessary plugins and gems.                           
`bundle exec jekyll s` is run for the first time, we can use `jekyll s` for next runs.                     

4. Create a Git repository without initializing .README                  

5. Upload to Github                  
Make sure to change your `baseurl` in `_config.yml` to your repo before upload.             

```
git init                          
git checkout -b gh-pages                            
git add .                        
git commit -m "initial commit"                         
git remote add origin git_repo_location                           
git push origin gh-pages                         
```

Check your blog status in Settings/ GitHub Pages.     

6. For the next commits:
```
git add .                        
git commit -m "initial commit"                         
git remote add origin git_repo_location                           
git push origin gh-pages       
```

# References
(Youtube)[https://youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB]