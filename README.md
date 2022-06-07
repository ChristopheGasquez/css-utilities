| Project | Version | Demo | Author | Repository | License |
|:---:|:----:|:----:|:----:|:----:|:----:|
| crispi-css-utilities | 1.0.0 | [css-utilities.crispi.app](https://css-utilities.crispi.app) | [Christophe Gasquez](https://www.linkedin.com/in/christophe-gasquez) | [Git Hub](https://github.com/ChristopheGasquez/css-utilities.git) | **ISC** |

# Crispi CSS Utilities

*Crispi Css Utilities* is a style micro framework that can be used in both scss and css.  
It provides classes respecting a naming formalism that can be easily deduced.  
You can customize the entire library to adapt it to your needs and your designs.

## Installation

### Node package **(recommended)**

Add the Node package to your project:

```shell script
$ npm i crispi-css-utilities --save
```

You can now use the library in your project in [SCSS mode](#use-in-scss-mode) 
or [CSS mode](#use-in-css-mode) and customize it to your liking.

### HTTP Deliver

Add the style sheet links that suit you (light, medium, complete, etc.) on your `<head>` tag.
```html
<link href="https://css-utilities.crispi.app/css/{{ styles.css }}" rel="stylesheet">
```

## Overall operation

Crispi CSS Utilities is a micro framework providing developers with a set of classes 
responding to a simple formalism:  
The name of the property in kebab case (example: `text-align`, 
followed by the expected value in kebab case (example: `center`, separated by a double dash `--`.

To center the text of a paragraph, you can therefore write:
```html
<p class="text-align--center">My centered paragraph</p>
```

If the list of properties corresponds strictly to that defined by the css standards, 
the list of values ​​is enriched.

Indeed, in addition to the fixed values ​​linked to the property,
'non-fixed' values ​​can be specified. 

> Example:
> The `word-spacing` property can take as a fixed value, one of the following values: `auto`, `initail`, `inherit`.
> However, it can be associated with a non-fixed value, such as a length in pixels `px` or ephemeral unit `em`).
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

### Importation

### Customize


## Use in SCSS mode

### Scripts

### Customize
