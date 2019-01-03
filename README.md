+++

+++

# Onepress

Onepress is a simple, clean, and responsive "Hugo - Static Site Generator" theme for bloggers.

## Features

- Simple, clean, and responsive
- Tags
- Sidebar widgets (optional)
- [Disqus](https://disqus.com/) comments
- Syntax highlighting with [Highlight.js](https://highlightjs.org/)
- [Font Awesome](https://fontawesome.io) Icons
- SEO-friendly construction
- [Google Analytics](https://analytics.google.com/)
- [OpenGraph](http://ogp.me/) and [Twitter Cards](https://dev.twitter.com/cards/overview) integration
- Custom CSS option
- Twitter and Facebook share button
- Author box (optional)

## Screenshot 

![]()

## Installation

### Option 1: Clone Repository

In the root of your Hugo site directory run:

```
$ cd themes
$ git clone https://github.com/ijsucceed/onepress.git
```

### Option 2: Create Submodule

Create a submodule linked directly to the theme's GitHub repository in order to receive updates:

```
$ git submodule add https://github.com/ijsucceed/onepress.git themes/onepress
```
Then run:

```
$ git submodule update --init --recursive --remote
```

## Configuration

Onepress comes with several configuration options to aid in site customization. This is an example `config.toml` file:


```
baseURL = "https://ijsucceed.com/"
languageCode = "en-UK"
title = "Onepress Example Site"
description = "a Blog by Jeremiah Succeed"
config = "config.toml"
tags = ["blog", "sidebar", "SEO"]
theme = "onepress"
# Enter your tracking code to enable Google Analytics
googleAnalytics = " "
# Disable comments by leaving disqusShortname empty
disqusShortname = "your disqus shortname"
copyright = "Copyright © 2019, Jeremiah Succeed; all rights reserved."
canonifyURLS = true
paginate = 12

[params]
	author = "Jeremiah Succeed"
    bio = "Fullstack web developer and Templates designer."
	logo = "/images/onepress-logo.png"
	avatar = "/images/onepress-author.png"
	opengraphImage = "/images/onepress-logo.jpg"
	enableRSS = true

	customCSS = false
    readMore = "Read Up"
    
    # Social
	twitter  = "ijsucceed"
	github   = "ijsucceed"
	facebook  = ""
    linkedin  = "ijsucceed"

    
    # Widget
    widgets = true
    
    # Author box and Share button
    authorCard = false 
    shareButton = true
    
    # Code highlighting with highlight.js
    highlightJS = true

# Taxonomies
[taxonomies]
    tag = "tags"

```

## Using Onepress

The two main content types are blog posts and sidebar widgets.

## Widgets

To create a widget section that renders on the sidebar, go to your `layouts/partials/` folder and locate `widgets.html`.

```
<div class="widgets">
      
  <section itemscope itemtype="https://schema.org/Person" class="widget socials">
    <h2 class="widget-title">Socials</h2>
    <ul>
    ....
    </ul>
  </section>
  <!-- You can add multiple widgets section below -->

</div>
```

The themes has a default widget which is used to display social icons.

You can simply add widget like this below.

```
  <section class="widget customwidget">
    <h2 class="widget-title">Widget Title</h2>
    // widget body
  </section>
```

Whatever content you put inside the widget should fit properly to the widget space. This can be ad, affliate banner or call to action.

You can also reorder the widgets simply by placing anyone section above the other.

Removing a widget is simply by commenting(with html comment) that particular widget *section* or remove the *section* code entirely.

### No sidebar

If you don't want a sidebar you can set the `widgets` to *false* in the `config.toml`. This will remove the sidebar and center your site content.

```
# Widget
widgets = false
```

## Blog Posts

To create a new blog post, run:

```
$ hugo new post/post-title.md
```

## Custom CSS

To implement custom CSS sitewide, change the config.toml parameter customCSS from false to true and then go to `css.html` file in your `layouts/partials/` folder and add a css code like the example below:

```
<style>
  <!-- This will remove the shadow on the navbar -->
  a {
    border-color: orange;
  }
</style>
```

This will render inline CSS in the head of your site and without adding an extra HTTP request.

## Contributions

If you'd like to help with the continous improvement of this theme, I encourage you to submit a pull request or create an issue if you find a bug. All help is celebrated.

## License

This theme is released under the MIT license. For more information read the [license](https://github.com/ijsucceed/onepress/blob/master/LICENSE).