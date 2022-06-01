# PicoCMS-blog-solarized-light-theme

A picoCMS blog theme with solarized light colors. Including tags, comments and toc.
Based on [the story Pico Theme](https://github.com/BesrourMS/story).


## Feature

A simple [picoCMS](https://github.com/picocms/Pico) theme :
+ Blog
+ Solarized Light theme
+ Comments
+ Tags
+ Table of content
+ Create diagrams using [mermaid-js](https://mermaid-js.github.io/mermaid/#/)

## Installation, Pico, version 2.x

To use this theme blog, you have to install it, and install 3 others plugins.

### Install the theme 

+ Clone this repo, or downoald it as a zip archive outside your `Pico` directory
+ Copy the content of the `solarizedLightBlog` directory in the `themes` folder of your **Pico** installation and change the following setting within your `config.yml`:

```yaml
theme:solarizedLightBlog 
logo: assets/myLogo.jpg
```

With the `logo` line, you will config the logo of your blog. It is **mandatory** to provide and config this logo as a 32x32 image (jpg or png).


### Tags

Use the [PicoTag](https://github.com/bricebou/PicoTags) plugin to add tags to your blog. You have just to make the installation part of the `README`. The templates of this blog has already been set to use this plugin. 
Then add the following line to your `config.yml`
```yaml
PicoTags.enabled: true
ptags:
  # Do you want to sort tags (case unsensitive) ?
  # true or false
  asort: true
  # Do you want to remove from the tags list
  # the ones that are used in only one page ?
  # true or false
  delunique: false
  # Specify the Twig template to use for the tag pages
  # The file has to be inside the theme in use folder
  # You have to indicate the ` `.twig` extension
  # See the template section into the README.md.
  template: tag.twig
  # This is a way to split the tag_list array in multiple arrays.
  # See the template section into the README.md for more info
  # on how to access them.
  nbcol: 1
  # Excluding pages from the tags list based on their template.
  # It has to be a string, with the `pipe (|)` as separator.
  # You have to escape single quotes with a backslash.
  # /!\ Be careful :
  # in some cases you can obtain 404 error
  # when there is no articles to display in a tag page.
  excluded_templates: "category|supcategory"
```

### TOC

We use the [TableOfContent](https://github.com/mcbSolutions/Pico-Plugins/blob/master/mcb_TableOfContent) plugin to generate table of content of each article.
+ Clone the [github.com/mcbSolutions/Pico-Plugins](https://github.com/mcbSolutions/Pico-Plugins) repo or download it as a zip archive outside your `Pico` directory. 
+ Copy the `mcb_TableOfContent` folder in your `plugins` directory.
+ The templates of this blog has already been set to use this plugin.
+ You can do the optional config.

### Comments

We use the [pico-comments](https://github.com/push-eax/pico-comments) plugin to add comments to the blog's article.
+ Clone the [github.com/push-eax/pico-comments](https://github.com/push-eax/pico-comments) repo or download it as a zip archive outside your `Pico` directory.
+ Copy the `PicoComments.php` file in a `PicoComments` folder in your `plugins` directory.
+ The templates of this blog has already been set to use this plugin.
+ add the following line to your `config.yml`
```yaml
PicoComments:
 # whether the comments plugin is enabled. comment data will not be available to Twig if this is false
 enabled: true
 # maximum character size of comments. comments larger than this will be rejected
 comment_size_limit: 40000
 # whether comments must be approved before displaying them to other users
 comment_review: false
```
### Plugin Directory

Your plugin directory should look like this:
```
mcb_TableOfContent  PicoComments  PicoDeprecated  PicoTags
```

## Usage

This theme provides 4 templates (twig) :
+ index : the left part of the homepage
+ single : all articles
+ simple : all other pages
+ tags : list of article by tag

### Index

It is **mandatory** to have a `index.md` in your `content` directory. It will appear on the left side of the homepage. 

### Article

```yaml
---
Template: single --> template for article
comments: true --> to allow comment, false to dissalow
Date: 2019-01-05 
title: Title of my article
Tags: projet,latex --> comma separated value (no space)
---
```

### Other pages 

You can also have other pages than index and articles by creating a markdown file in your `content` directory with the *simple* template.

```yaml
---
title: The title of my page
Template: simple
---
```
### Social network links

You can add 3 links (with logo) to social networks (twitter, LinkedIn and github) below the #tag list. Add this to your `config.yml`
```yaml
linkedin: https://my_linkedIn_url
twitter: https://my_twitter_url
github: https://my_github_url

```


## Demo

demo : [pico-solarized-light-blog.web-en-royans.fr](http://pico-solarized-light-blog.web-en-royans.fr/)

## Thanks

+ [the story Pico Theme](https://github.com/BesrourMS/story)
+ [Solarized CSS](https://thomasf.github.io/solarized-css/)
+ [github.com/mcbSolutions/Pico-Plugins](https://github.com/mcbSolutions/Pico-Plugins) 
+ [pico-comments](https://github.com/push-eax/pico-comments)
+ [PicoTag](https://github.com/bricebou/PicoTags)
