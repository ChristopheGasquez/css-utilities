| Project | Version | Demo | Author | Repository | License |
|:---:|:----:|:----:|:----:|:----:|:----:|
| crispi-css-utilities | 1.0.0 | [css-utilities.crispi.app](https://css-utilities.crispi.app) | [Christophe Gasquez](https://www.linkedin.com/in/christophe-gasquez) | [Git Hub](https://github.com/ChristopheGasquez/css-utilities.git) | **ISC** |

# Crispi CSS Utilities

*Crispi Css Utilities* is a style micro framework that can be used in both SCSS and CSS.  
It provides classes respecting a naming formalism that can be easily deduced.  
You can customize the entire library to adapt it to your needs and your designs.

## Installation

### Node package *(recommended)*

Add the Node package to your project:

```shell script
$ npm i crispi-css-utilities --save
```

You can now use the library in your project in [CSS mode](#use-in-css-mode) 
or [SCSS mode](#use-in-scss-mode) and customize it to your liking.

### HTTP Deliver *(not recommended)*

Add the style sheet links that suit you (`light`, `medium` or `complete`) on your `<head>` tag.
```html
<!-- {{ version }} must be replace by the version name( light, medium or complete). -->
<link href="https://css-utilities.crispi.app/css/{{ version }}.styles.css" rel="stylesheet">
```

### Choice of versions

*Crispi Css Utilities* provides you with three versions of its style sheets: `light`, `medium` and `complete`:

- The `light` version contains a limited number of properties. 
  These are the most common properties.
  It is a version quite suitable for small projects wanting to be fast and light.
- The `medium` version contains a large part of the properties available in CSS
  and makes it possible to meet the majority of needs.
  This is the recommended version for the majority of projects.
- The `complete` version provides the exhaustive list of CSS properties available. 
  Some of them are uncommon. It is also the heaviest version.
  This version is only recommended for projects requiring uncommon CSS rules, 
  or for testing or learning purposes.

## Overall operation

*Crispi CSS Utilities* is a micro framework providing developers with a set of classes 
responding to a simple formalism:  
The name of the property in kebab case (example: `text-align`), 
followed by the expected value in kebab case (example: `center`), separated by a double dash `--`.

> Example: To center the text of a paragraph, you can therefore write:
> ```html
> <p class="text-align--center">My centered paragraph</p>
> ```

If the list of properties corresponds strictly to that defined by the CSS standards, 
the list of values ​​is enriched.

Indeed, in addition to the fixed values ​​linked to the property,
'non-fixed' values ​​can be specified. 

> Example:
> The `word-spacing` property can take as a fixed value, one of the following values: `auto`, `initail`, `inherit`.
> However, it can be associated with a non-fixed value, such as a length in pixels `px` or ephemeral unit `em`.
> ```html
> <p class="word-spacing--length-10px">My centered paragraph</p>
>  ```

All non-fixed values ​​are added as `custom properties` and can therefore be modified at any time
using the pseudo-selector `:root`.
They respect the standard nomenclature: double dash followed by the name of the value (example: `--primary`).

We have broken down non-fixed values ​​into five categories:
- [Colors](#colors-variables) broken down into three sub-lists:
    [main](#main-colors), [status](#status-colors), [shade](#shade-colors);
- [Fonts](#font-variables);
- [Integers](#integer-variables) broken down into two sub-lists: 
    [decimals](#decimals), [integers](#integers);
- [Sizes](#size-variables) broken down into seven sub-lists: 
    [ephemeral units](#ephemeral-units), [pixels](#pixels), [borders](#borders), [containers](#containers), 
    [font-sizes](#font-sizes), [gaps](#gaps), [percents](#percents);
- [Times](#time-variables).

### Colors variables
Three color lists can be used: [main colors](#main-colors), 
[status colors](#status-colors) and [shade colors](#shade-colors).

#### Main colors
The main colors are:
- `light` *with default value `#efefef`*,
- `dark` *with default value `#242424`*,
- `primary` *with default value `#157e82`*,
- `secondary` *with default value `#154a82`*,
- `tertiary` *with default value `#15824f`*,
#### Status colors
The status colors are:
- `info` *with default value `#2875c6`*,
- `success` *with default value `#3bbf4f`*,
- `warning` *with default value `#faa701`*,
- `danger` *with default value `#861010`*,
- `default` *with default value `#666666`*,
#### Shade colors
The shade colors are:
- `shade-100` *with default value `lighten($dark, 90%)`*,
- `shade-200` *with default value `lighten($dark, 80%)`*,
- `shade-300` *with default value `lighten($dark, 70%)`*,
- `shade-400` *with default value `lighten($dark, 60%)`*,
- `shade-500` *with default value `lighten($dark, 50%)`*,
- `shade-600` *with default value `lighten($dark, 40%)`*,
- `shade-700` *with default value `lighten($dark, 30%)`*,
- `shade-800` *with default value `lighten($dark, 20%)`*,
- `shade-900` *with default value `lighten($dark, 10%)`*,

### Font variables
The list of fonts is:
- `f-primary` *with default value `hevetica`*,
- `f-secondary` *with default value `verdana`*,
- `f-tertiary` *with default value `arial`*,

### Integer variables
Two integer lists can be used: [decimals](#decimals) and [integers](#integers).

#### Decimals
The list of decimals is:
- `dec-1` *with default value `.1`*,
- `dec-2` *with default value `.2`*,
- `dec-3` *with default value `.3`*,
- `dec-4` *with default value `.4`*,
- `dec-5` *with default value `.5`*,
- `dec-6` *with default value `.6`*,
- `dec-7` *with default value `.7`*,
- `dec-8` *with default value `.8`*,
- `dec-9` *with default value `.9`*,

#### Integers
The list of integers is:
- `int-1` *with default value `1`*,
- `int-2` *with default value `2`*,
- `int-3` *with default value `3`*,
- `int-4` *with default value `4`*,
- `int-5` *with default value `5`*,
- `int-6` *with default value `6`*,
- `int-7` *with default value `7`*,
- `int-8` *with default value `8`*,
- `int-9` *with default value `9`*,
- `int-10` *with default value `10`*,

### Size variables
Six size lists can be used: [ephemeral units (em)](#ephemeral-units), [pixels (px)](#pixels), 
[borders](#borders), [containers](#containers), [font-sizes](#font-sizes), [gaps](#gaps) and [percents](#percents).

#### Ephemeral units
The list of ephemeral units is:
- `length-05em` *with default value `.5em`*,
- `length-075em` *with default value `.75em`*,
- `length-1em` *with default value `1em`*,
- `length-2em` *with default value `2em`*,
- `length-3em` *with default value `3em`*,
#### Pixels
The list of pixels is:
- `length-0` *with default value `0`*,
- `length-1px` *with default value `1px`*,
- `length-2px` *with default value `2px`*,
- `length-3px` *with default value `3px`*,
- `length-5px` *with default value `5px`*,
- `length-10px` *with default value `10px`*,
- `length-20px` *with default value `20px`*,
- `length-30px` *with default value `30px`*,
- `length-50px` *with default value `50px`*,
- `length-75px` *with default value `75px`*,
- `length-100px` *with default value `100px`*,
- `length-150px` *with default value `150px`*,
- `length-200px` *with default value `200px`*,
- `length-300px` *with default value `300px`*,
- `length-400px` *with default value `400px`*,
- `length-500px` *with default value `500px`*,
#### Borders
- `border-size-xs` *with default value `.1rem`*,
- `border-size-sm` *with default value `.2rem`*,
- `border-size-md` *with default value `.4rem`*,
- `border-size-lg` *with default value `.7rem`*,
- `border-size-xl` *with default value `1rem`*,
- `border-size` *with default value `$border-size-md`*,
#### Containers
The list of containers is:
- `container-xs` *with default value `375px`*,
- `container-sm` *with default value `650px`*,
- `container-md` *with default value `820px`*,
- `container-lg` *with default value `1180px`*,
- `container-xl` *with default value `1400px`*,
- `container` *with default value `$container-md`*,
- `container-full` *with default value `100%`*,
#### Font sizes
The list of sizes is:
- `font-size-xs` *with default value `.5rem`*,
- `font-size-sm` *with default value `.75rem`*,
- `font-size-md` *with default value `1rem`*,
- `font-size-lg` *with default value `2rem`*,
- `font-size-xl` *with default value `3rem`*,
- `font-size` *with default value `$font-size-md`*,
#### Gaps
The list of gaps is:
- `gap-xs` *with default value `.5rem`*,
- `gap-sm` *with default value `1rem`*,
- `gap-md` *with default value `1.5rem`*,
- `gap-lg` *with default value `2rem`*,
- `gap-xl` *with default value `3rem`*,
- `gap` *with default value `$gap-md`*,
#### Percents
The list of percents is:
- `percent-0` *with default value `0%`*,
- `percent-10` *with default value `10%`*,
- `percent-20` *with default value `20%`*,
- `percent-30` *with default value `30%`*,
- `percent-40` *with default value `40%`*,
- `percent-50` *with default value `50%`*,
- `percent-60` *with default value `60%`*,
- `percent-70` *with default value `70%`*,
- `percent-80` *with default value `80%`*,
- `percent-90` *with default value `90%`*,
- `percent-100` *with default value `100%`*,

### Time variables

The list of times is:
- `duration-01` *with default value `.1s`*,
- `duration-05` *with default value `.5s`*,
- `duration-1` *with default value `1s`*,
- `duration-2` *with default value `2s`*,
 
## Use in CSS mode

We recommend using [SCSS mode](#use-in-scss-mode). But if you don't want to compile your style sheets, 
and only use CSS technology, you can still use and customize *Crispi CSS Utilities*.

### CSS importation

You can either use the CSS stylesheets stored on our servers (not recommended), 
or add our CSS stylesheets to your project via npm, or by downloading them from our 
[github repository](https://github.com/ChristopheGasquez/css-utilities.git).

> Example: Import directly from *Crispi* servers
> ```html
> <!-- {{ version }} must be replace by the version name( light, medium or complete). -->
> <link href="https://css-utilities.crispi.app/css/{{ version }}.styles.css" rel="stylesheet">
> <link href="{{your-project-name}}/css/your-project-styles.css" rel="stylesheet">
> ```
> Import from your project:
> ```html
> <link href="{{your-project-name}}/css/crispi-css-utilities.css" rel="stylesheet">
> <link href="{{your-project-name}}/css/your-project-styles.css" rel="stylesheet">
> ```

### CSS customizations

By importing your stylesheet after *Crispi CSS Utilities*, you will be able to modify all customs properties 
using the `:root` pseudo selector. 
If you import our style sheet after ours, only custom property modifications with a stronger selector 
will be taken into account (example: `body:root { /*Your custom propertie modifications*/ }`).

> Example: To modify the colors associated with the main color, you can:
> ```css
> :root {
>   --ligth: #25002b;
>   --dark: #f6dcfa;
>   --primary: #a800c4;
>   --secondary: #9bc400;
>   --tertiary: #0081c4;
> }
> ```

With this simple declaration, all the classes of *Crispi CSS Utilities* will be in the colors of your project!  
In addition to [colors](#colors-variables), you can modify the non-fixed [fonts](#font-variables), 
[integers](#integer-variables), [sizes](#size-variables) and [times](#time-variables) values 
to tune your design as precisely as possible.

## Use in SCSS mode

We recommend that you integrate *Crispi CSS Utilities* into your project in SCSS mode. 
Thus, you can modify the variables before creating the custom properties, 
but also use the functions and mixins of the library to enrich and factorize your own code.
The most experienced users can also create their own versions of *Crispi CSS Utilities* 
by generating only the classes that interest them, associated with the desired names and values 
(show: [SCSS customization](#scss-customizations)).

### SCSS importations

You can import *Crispi CSS Utilities* directly into your SCSS stylesheet.
Thus, you can both modify the variables used by the libraries, 
but also use the functions and mixins that it makes available to you.

Import the library (with `@import`), choosing the desired version: `light`, `medium` or `complete`. 
Functions, mixins and customization are available in all versions.

> Example: To add the complete version to your stylesheet
> ```scss
> @import 'node_modules/css-utilities/scss/complete.styles.scss';
> ```

The library is built into your project and compiled by your scss interpreter.
So you can both use it in your style sheet, but also in the html page that imports your compiled CSS file.


### SCSS customizations

You can customize your styles in the same way as with the CSS mode, 
using the custom property. See the part: [CSS customization](#css-customizations).

You can also customize your styles thanks to the scss variables. 
*Crispi CSS Utilities* SCSS variables are all set to `!default`, 
so you can override them with your own values. 
For them to be taken into account during compilation, 
define them before importing the *Crispi CSS Utilities* styles.

> Example: To change the primary color, do...
> ```scss
> $primary: yellow;
> 
> @import 'node_modules/ncss-utilities/scss/medium.styles.scss';
> ```

Because all non-fixed values inherit from an SCSS variable marked as `!default`, 
you can easily deduce all of these variables and their custom properties.

> Example: For non-fixed value `container-xs`  
> ```scss
> // You can deduct that associated scss variable:
> $container-xs: 375px !default;
>  
> // You can deduct that associated custom property
> :root {
>   --container-xs: $container-xs;
> }
> 
> // The list of variables associated with container values will also contain
> // a container-xs property associated with the custom property --container-xs
> $container-list: (
>   'container-xs': var(--container-xs)
> )
> ```

So, by overriding the original `$container-xs` variable, 
you are also overriding the associated custom property as well as its reference in the parent list.

Finally, you can use the functions and mixins of *Crispi CSS utilities* 
to add your own CSS classes to your final stylesheet.

> Example: To create your abbreviated background color classes:  
> ```scss
> @import 'node_modules/css-utilities/scss/tools';
> 
> @include classesGenerator(('bkc': background-color), fromListToMap(red, blue));
> ```
> After compiling:
> ```css
> .bkc--red {
>   background-color: red;
> }
> .bkc--blue {
>   background-color: blue;
> }
> ```

## Library structure

```markdown
/crispi-css-utilities
|-- /src
|   |-- /css
|   |   |-- complete.styles.css
|   |   |-- light.styles.css
|   |   |-- medium.styles.css
|   |   |-- styles.css
|   |
|   |-- /scss
|   |   |-- /constants
|   |   |   |-- _index.scss
|   |   |   |-- _property-key-pairs.scss
|   |   |   |-- _property-value-pairs.scss
|   |   | 
|   |   |-- /factories
|   |   |   |-- _css.complete.scss
|   |   |   |-- _css.light.scss
|   |   |   |-- _css.medium.scss
|   |   |
|   |   |-- /tools
|   |   |   |-- _functions.scss
|   |   |   |-- _index.scss
|   |   |   |-- _mixins.scss
|   |   |
|   |   |-- /variables
|   |   |   |-- _colors.scss
|   |   |   |-- _fonts.scss
|   |   |   |-- _index.scss
|   |   |   |-- _integers.scss
|   |   |   |-- _sizes.scss
|   |   |   |-- _times.scss
|   |   |
|   |   |-- complete.styles.scss
|   |   |-- light.styles.scss
|   |   |-- medium.styles.scss
|   |   |-- styles.scss
|   |
|   |-- index.html
|
|-- package.json
|-- package-lock.json
|-- README.md
```
