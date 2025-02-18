# Life in Weeks
My Version

Read more about [Life in Weeks at Wait But Why](https://waitbutwhy.com/2014/05/life-weeks.html).

This code was copied and adapted from [Gina Trapani](https://weeks.ginatrapani.org/) who copied [Buster Benson](https://busterbenson.com/life-in-weeks). It is a single webpage statically-rendered with [Hugo](https://gohugo.io/) hosted on Netlify. It consists of two [data](data/events.yml) [files](data/colors.yml), [an introduction](content/index.md), and a [template](layouts/_default/index.html).

## 🚀 Setup

1. Install Hugo:
   ```sh
   brew install hugo  # Mac
   ```
2. Clone and run locally:
```sh
    git clone https://github.com/ginatrapani/life-in-weeks.git
    cd life-in-weeks
    hugo server -D
```
3. Visit [http://localhost:1313/](http://localhost:1313/).

## ✨ Customize

- `content/` → Page content
- `layouts/` → Templates
- `assets/scss/` → Styles
- `assets/imgs/` → Site-wide images
- `static/` → Unprocessed assets
- `hugo.toml` → Site settings

## Colophon

This page uses [Bootstrap](https://getbootstrap.com/) for layout and interaction, and a smidge of [jQuery](https://jquery.com/) to reflect the current week on the map.

The font is [Red Hat Display](https://fonts.google.com/specimen/Red+Hat+Display). Colors chosen via [Color Hunt](https://colorhunt.co/). Edited in [Zed](https://zed.dev).

## More Life in Weeks

There are several neat Life in Weeks examples and tools, including:

- [Weeksofyour.life](https://www.weeksofyour.life/): Make your own, completely browser-based
- [Life Calendar](https://lifecalendar.io): Make your own, with multiple layers
- [My Life in Days](https://days.sonnet.io/): Beautiful refactor, by days

🍯 “I always get to where I am going by walking away from where I have been.” – Winnie the Pooh

## 
```
{
  "scripts": {
    "build": "hugo --gc --minify",
    "start": "hugo server --disableFastRender"
  }
}

{
    "version": 2,
    "builds": [
        {
        "src": "life-in-weeks/*",
        "use": "@vercel/static-build",
            "config": {
                "distDir": "public"
            }
        }
    ],
    "routes": [
        {
        "src": "/(.*)",
        "dest": "/public/$1"
        }
    ]
}


```
