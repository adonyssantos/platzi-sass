# Useful Sass Template

[Sass](https://sass-lang.com/) is the most mature, stable, and powerful professional grade CSS extension language in the world.

Sass is completely compatible with all versions of CSS. We take this compatibility seriously, so that you can seamlessly use any available CSS libraries.

The style file extensions will be `.scss`. \
Use `_` at the beginning of any `.scss` file so it won't compile.

I made this template for future projects I do using Sass.

## Get starter

1. Create a repository from this template.
2. Clone the repository in your PC.
3. Install the modules with `npm install`.
4. Now you can use the [scripts](#scripts) to compile the Sass files.

## Scripts

This project runs on `node.js`. Install [Node](https://nodejs.org/) for npm to use.

Run `npm install` in the project directory and make sure it passes.

In this project you can run the following Scripts:

### `npm css-compile`

Compile all the sass code into the `./src/scss/` folder. \
Use `_` at the beginning of any `.scss` file so it won't compile.

### `npm run css-minify`

Does the same as `npm css-compile` and then minifies the compiled files. \
This is very useful when uploading a file to production.

## Credits

This project is created from [Sass Boilerplate](https://github.com/KittyGiraudel/sass-boilerplate.git).
