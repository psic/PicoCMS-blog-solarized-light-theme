# PicoCMS-blog-solarized-light-them
A picoCMS blog theme with solarized light colors. Including tags, comments and toc

## Feature

A simple [picoCMS](https://github.com/picocms/Pico) theme :
+ 3 configurable colors.
+ First level title show in menu.
+ Optional 3 columns footer.
+ Tagline in header.

## Installation, Pico, version 2.x

Copy the content of the `3colors` directory in the `themes` folder of your **Pico** installation and change the following setting within your `config.yml`:

```yaml
theme:solarizedLightBlog 
```
## Usage

### Title and tagline

+ Title : the site title is written in the `config.yml' file and will we be shown as a H1 tag in your header.
```yaml
site_title: 3 colors
```
+ tagline : your tag line is written in the `_meta.md` file of your `content` folder. It will be shown as a H2 tag in your header.
```yaml
Tagline: Choose 3 colors <br> Show your H1 in menu
```

### 3 colors

You can configure 3 colors in the theme using the `_meta.md` file of the `content` folder : the decoration color - color1 - (link hover, horizontal line, header,...), the body background color  - color2 - and the main section background color -color3 -.
```yaml
color1: rgb(57,0,64)
color3: rgb(194,192,148)
color2: rgb(169,165,135)
```
Use rgb format color or string color (blue, gree, lightgrey, ...), but no hex color code.

### 3 columns footer

You can have a 3 columns footer. If no column is define, then the footer is not shown. The footer has 3 columns (width : 20%, 60%, 20%). It is define in the `_meta.md` file in the `content` folder.
```yaml
footerCenter: Fortunae mercatoribus ad Anthemusia in.
footerRight: Qui sunt debent ob non.
footerLeft: Graecia pro quaedam argutiis): nimis.
```

## Demo

demo : [pico-solarized-light-blog.web-en-royans.fr](http://pico-solarized-light-blog.web-en-royans.fr/)

