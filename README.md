# Phlogiston

[![Build Status](https://travis-ci.org/RedMike/phlogiston.svg?branch=master)](https://travis-ci.org/RedMike/phlogiston)

Phlogiston is a simple website template built for portfolio/blog websites. Its main goal is to provide a good base to start off from for user modifications that correspond to your own use cases.

This theme was created from scratch, with responsiveness and modern HTML features in mind.

![screenshot](screenshot) ![screenshot-mobile](screenshot-mobile)


## Features

* Responsive design, partially implemented using flexbox
* Override-able partial templates for extending with custom elements
* Disqus integration for comments
* Google Analytics integration
* Text-based social icons ([FontAwesome](https://fontawesome.com) or similar required)


## Installation

Download and install [Hugo](https://gohugo.io/overview/installing/) and run (if on Linux):

```sh
$ mkdir themes
$ cd themes
$ git clone https://github.com/RedMike/phlogiston
```

## Disqus integration

Disqus is integrated with Hugo natively, and only requires that you set

```toml
disqusShortname = "short-name"
```

in your config.toml file.


## Configuration

There are a number of custom parameters available in config.toml, as well as partial templates that can be overriden.


### Global

```toml
[[Params.customCss]]
  url = "/css/custom.css"
[[Params.customCss]]
  url = "https://example.com/custom.css"
[[Params.customJs]]
  url = "/js/custom.js"
[[Params.customJs]]
  url = "https://example.com/custom.js"
```

The above options allow you to include custom CSS or JS to your site. These will be included on every page. Repeat the elements in order to include multiple.


### Sidebar

```toml
Image120 = "/link/to/image"
Image240 = "/link/to/bigger/image"
```

The above options control the image displayed on the sidebar. Omitting them stops the image from displaying.

```toml
Description = """Your description here, in *Markdown*."""
```

The above option controls the description underneath the site name. This supports all Markdown elements.

`layouts/partials/sidebar-extra.html` can be created in your own website in order to add custom HTML/JS to the sidebar, below the description.

```toml
[[Params.socialIcons]]
  iconClass = "fa fa-github-square"
  url = "https://github/Example"
```

The above option allows you to add social icons to the bottom of your sidebar. Create multiple elements to add multiple icons. You will have to import FontAwesome, or similar services, to your site in order to use this.


### Navbar

```toml
Navbar = true
```

The above option enables a built-in top navigational menu with links to categories of posts.

```toml
NavbarCategories = ["post", "project"]
```

The above option allows you to control which categories show up in the menu.


### Front Page

```toml
FrontPageCategories = ["post"]
```

The above option allows you to control which categories are shown on the main page.

`layouts/partials/front-header.html` can be created in your own website in order to add custom HTML/JS to the top of the home page, below the navbar.


## License

This theme is released under the MIT license.


[screenshot]: https://raw.githubusercontent.com/RedMike/phlogiston/master/images/screenshot.png
[screenshot-mobile]: https://raw.githubusercontent.com/RedMike/phlogiston/master/images/screenshot-mobile.png