# PrimeNG Theming with SASS
# Custom Theme

Themes are created with SASS using the `primeng-sass-theme` project available at [github](http://github.com/primefaces/primeng-sass-theme). This repository contains all the SCSS files for the components and the variables of the built-in themes so that you may customize an existing theme or create your own. The SCSS variables used in a theme are available at the [SASS API](https://www.primefaces.org/designer/api/primeng/15.0.0) documentation.

There are 2 alternatives to create your own theme. The first option is compiling a theme with command-line sass whereas the second option is embedding SCSS files within your project to let your build environment do the compilation. In all cases, the generated theme file should be imported to your project.

## Theme SCSS

The theme SCSS is available as open source at [primeng-sass-theme](http://github.com/primefaces/primeng-sass-theme) repository. The `theme-base` folder contains the theming structure of the components, themes under `themes` folder import the base and define the SCSS variables. The `themes` folder also contains all the built-in themes so you can customize their code as well.

To create your own theme, [download](https://github.com/primefaces/primeng-sass-theme/releases) the release matching your PrimeNG version and access the `themes/mytheme` folder. The SASS variables to customize are available under the `variables` folder. The `_fonts` file can be used to define a custom font for your project whereas the optional `_extensions` file is provided to add overrides to the components designs. The `theme.scss` file imports the theme files along with the `theme-base` folder at the root to combine everything together. The next step would be the compilation of the SCSS that can either be command-line or within your project.

## Compile SCSS Manually

Once your theme is ready, run the following command to compile it. Note that [sass](https://www.npmjs.com/package/sass) command should be available in your terminal.

```bash
sass --update themes/mytheme/theme.scss:themes/mytheme/theme.css
```

Then copy and import the `theme.css` file in your application. For example, in Angular CLI, you may place `theme.css` under the assets folder and then import it in `styles.css`.

```css
@import 'assets/theme.css';
```

