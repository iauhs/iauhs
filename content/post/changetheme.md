+++
date = "2016-02-15T23:46:38+01:00"
description = "change the theme to slender"
keywords = ['change theme hugo']
title = "How to change the theme"

+++



# How to change the theme?
参考网页 ： 

1. [The theme slender](http://themes.gohugo.io/slender/)
1. [Using a Theme](https://gohugo.io/themes/usage/)

---

首先在`theme/`文件夹中下载所需的theme ：

```
git clone https://github.com/CrimsonRay/slender
```
更改`config.toml`文件 ：

```
# config.toml
# https://github.com/CrimsonRay/slender

baseurl = "http://url-to-your-site.com/"
title = "Your Title"
languageCode = "en-US"
MetaDataFormat = "toml"
theme = "slender"
paginate = 3
PaginatePath = "/"

[author]
    name = "Your Name"

[permalinks]

    # Permalink format for pages.
    page = "/:title/"

    # Permalink format for blog posts.
    post = "/article/:title/"

[params]

    # Change the color scheme of Slender.
    # See above for preview and list of color schemes.
    colorscheme = "white"

    # Tagline; HTML accepted here. Keep it concise.
    tagline = "Your Tagline"

    # Footer; Markdown accepted here.
    footer = "Copyright 2015 &copy; Your Name"

    # Description and keywords for <meta> tags.
    # Remember to set this for your main page.
    # This will be overridden by whatever is set by the page or post,
    # defined by `description` and `keywords` variables in the front matter
    # of the markdown file.
    description = "Default Page Description"
    keywords = "default,page,keywords"

    # Social links, must be full URLs (e.g. https://github.com/CrimsonRay/).
    # Remove, comment, or leave blank any field to leave them out.
    email = "mailto:your-email"
    github = "url-to-your-github"
    bitbucket = "url-to-your-bitbucket"
    twitter = "url-to-your-twitter"
    stackoverflow = "url-to-your-stackoverflow"
    linkedin = "url-to-your-linkedin"
    facebook = "url-to-your-facebook"

    # Google Analytics
    # Remove, comment, or leave it blank if you don't have one.
    ganalytics = "your-google-analytics-tracking-code"

[menu]

    # Menu for the nav bar.
    # There must always be one item present (e.g. home).
    [[menu.main]]
    identifier = "home"
    name       = "home"
    url        = "/"
    weight     = 0

    [[menu.main]]
    identifier = "about"
    name       = "about"
    url        = "/about/"
    weight     = 1

```


然后再运行下面的命令

```

hugo -t ThemeName

hugo

./deploy.sh  
```

就可以了 :)