# Casper Photo

Fork of [Casper](http://github.com/tryghost/casper/) (the default included theme for [Ghost](http://github.com/tryghost/ghost/)), improved for photo blogs.

![Casper Photo screenshot](assets/screenshot-desktop.jpg?raw=true)

## Fork differences

- Removed the large card in the "grid view" so always displays 3 images/posts per row
- Maintain the aspect ratio of images (not forced to 200px high)
- Display featured images from posts only, no date, author, or tags (still shows these within the post view)
- Removed reading time display from posts
- Miscellaneous style changes

## Installing

Download the latest .zip from the [releases](https://github.com/DJM0/CasperPhoto/releases) page.

Then within your Ghost site navigate to *setting* > *design* (`/ghost/#/settings/design`) and upload the .zip using the *Upload a theme* button, then click *ACTIVATE*.

## Development

Casper Photo styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# install dependencies
yarn install

# run development server
yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/casper-photo.zip`, which you can then upload to your site.

```bash
# create .zip file
yarn zip
```
