# Penny

> a minimalist hugo theme

<img src="https://github.com/davidwinter/penny/raw/main/static/penny.jpg" width="250" alt="Penny" style="border-radius: 250px;"/>


## Setup

Clone this repo into your `themes` directory:

```sh
git clone https://github.com/davidwinter/penny.git themes/penny
```

And update your hugo project config file to include:

```yml
theme: penny
```

## Configuration

Penny tries to be as configurable as possible and a number of partial templates, site params and a main menu allow you to change the theme to suit your needs with as minimal effort as possible.

### Partial templates

The following partials can be overridden to add additional content to your website:

- `partials/head_additional.html` - included before the close `</head>` tag
- `partials/header_additional.html` - included before the `main` content block
- `partials/footer_additional.html` - included before the "back to top" arrow
- `partials/footer_credit.html` - the theme credit at the bottom of each page

These can be located within `layouts/partials` of your hugo project directory.

### Params

The site parameters are used:

- `image` - the image to be displayed at the top of all pages. Ensure it is a square image so it appears within a circle and located within the `static` directory
- `image_alt` - the alt text for the header image
- `title` - the title of your site
- `description` - the description of your site. Used in `<head>` meta tags and Open Graph and Twitter meta tags
- `homePageKinds` - an array of kinds of pages that you want included on the homepage listing.

Defaults for the above parameters are as follows:

```yml
params:
  image: penny.jpg
  image_alt: Photo of Penny
  title: Penny
  description: a minimalist hugo theme
  homePageKinds:
    - post
    - posts
```

### Menus

The menu displayed at the top of the website is labelled `main` so within your site config file, use something similar to:

```yml
menu:
  main:
    - identifier: about
      name: About
      url: /about/
      weight: 0
    - identifier: twitter
      name: Twitter
      url: https://twitter.com/<your username>
      weight: -1
    - identifier: github
      name: GitHub
      url: https://github.com/<your username>
      weight: -2
    - identifier: instagram
      name: Instagram
      url: https://instagram.com/<your username>
      weight: -3
    - identifier: linkedin
      name: LinkedIn
      url: https://uk.linkedin.com/public-profile/in/<your username>
      weight: -4
```
