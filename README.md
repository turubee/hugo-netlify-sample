hugo-netlify-sample
===

# Environment
- macOS
- homebrew

# How to

## Install Hugo
```
$ brew install hugo
```

## Create Site Project
```
$ hugo new site hugo-netlify
```

## Download Theme
https://themes.gohugo.io/  
```
$ git submodule add https://github.com/crakjie/hugo-base-theme.git themes/hugo-base-theme
```

## New Post
```
$ hugo new hello.md
$ echo hello >>content/hello.md
```

## Run local
```
$ hugo server --buildDrafts --theme=hugo-base-theme
                   | EN
+------------------+-----+
  Pages            |   5
  Paginator pages  |   0
  Non-page files   |   0
  Static files     | 110
  Processed images |   0
  Aliases          |   0
  Sitemaps         |   1
  Cleaned          |   0

Total in 48 ms
Watching for changes in /Users/xxxx/work/hugo-netlify/{content,data,layouts,static,themes}
Watching for config changes in /Users/xxxx/work/hugo-netlify/config.toml
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```

http://localhost:1313/  
http://localhost:1313/hello/  

## Config
```
$ sed -i '' "s/http:\/\/example.org\//https:\/\/turubee-hugo-netlify-sample.netlify.com\//" config.toml
```

## Push Github
First, create a repository with github  

```
$ echo /public >.gitignore
$ git init
$ git add .
$ git commit -m 'first commit'
$ git remote add origin git@github.com:turubee/hugo-netlify-sample.git
$ git push origin master
```

