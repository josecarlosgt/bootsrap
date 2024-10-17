# Lab Engagement Practice: Bootstrap Basics

In this practice, we will use the front-end development framework [Bootstrap](https://getbootstrap.com/), one of the most popular frameworks for styling websites. 

Each task below contains links to [Bootstrap official documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/). The purpose of this tutorial is to let you familiarize yourself with Bootstrap's documentation and apply Bootstrap's predefined CSS classes to style your website.

### Download the resources

We will work with a design inspired by the [New Age](https://startbootstrap.com/previews/new-age) template from the [Start Bootstrap](https://startbootstrap.com/) website.

Download the base code from [here](https://github.com/josecarlosgt/bootstrap/raw/practice-responsive-design/base.zip). We will work with the **index.html** file and the images included in the assets directory.

[Link to the page narrative](https://docs.google.com/document/d/1tnplJskdtc41upRjyfd3wu_NzxDQAH3-NoEJXKJdbco/edit?usp=sharing)

Link to the mockup designs:
- [Main page](https://drive.google.com/file/d/1R7fQwVBQPnJ3DMpoc4sUJmozKeDux1HM/view?usp=sharing)
- [Main page with modal window](https://drive.google.com/file/d/1iaGfRBPpbkQHqXAf56o62qmWy_FzNQh8/view?usp=sharing)


## Task 1: Page's settings and introduction

Let's first specify the page's title and meta description with the content provided in the page narrative:

```html
<title>[PAGE TITLE]</title>
<meta name="description" content="[DESCRIPTION]" />
```

## Task 2: Install Bootstrap
Reference: [Bootstrap Docs > Introduction](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

The easiest way to add Bootstrap to your website is by using the content delivery network (CDN) servers recommended by Boostrap. Other approaches require downloading the source files, which allows higher customization.

We will use the CDN resources:
- Include the CSS resource into the \<head\> element
- Include the JavaScript resource right before the closing body tag (</body>)
- You also need to include a [responsive meta tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag), which ensures proper rendering of your webpage on mobile devices. This is necessary because Bootstrap automatically optimizes your code for mobile devices.

Put it all together, and your webpage should look like this:
```html
<!doctype html>
<html lang="en">
    <head>
    ...
       
        <!-- Responsive metatag -->    
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- Bootstrap CSS -->
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
    </head>
    <body>
        ...
        <!-- Bootstrap JavaScript -->
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz" crossorigin="anonymous"></script>
  </body>
</html>       
```

> Learn more about the [integrity \(subresource integrity\)](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) and [crossorigin](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/crossorigin) attributes.

## Task 3: Styling text content

### Reboot: [Bootstrap Docs > Content > Reboot](https://getbootstrap.com/docs/5.3/content/reboot/)

When you start using Bootstrap out of the box, it applies a reboot of the default browser styles. This means Bootstrap strips out all the default styles like margin, padding, font styles, and size, replacing them with a clean and basic set of default Bootstrap styles. The purpose of this reboot is to resolve inconsistencies across browsers and provide you with a simple baseline to build upon the style of your website that is consistent across browsers.  

### Typography: [Bootstrap Docs > Content > Typography](https://getbootstrap.com/docs/5.3/content/typography/)

Bootstrap also provides several features for styling text content that allow you to create customized headings, paragraphs, and lists.

The feature [display headings](https://getbootstrap.com/docs/5.3/content/typography/#display-headings) allows you to display your headings in a larger, slightly more prominent style.

Add "display-2" to h1, "display-5" to h2 elements:

```html
<h1 class="display-1">...</h1>
<h2 class="display-5">...</h2>
```
> Note that the display heading classes use a numbering independent of the HTML heading elements. The display headings classes can be used with any HTML element.

The feature [lead](https://getbootstrap.com/docs/5.3/content/typography/#lead) allows you to make paragraphs stand out. We can use this feature for the first paragraph on our website to make it look slightly bigger and more relevant than the rest of the paragraphs.

Apply the *lead* class to the paragraphs in the header and transparency sections:

```html

<p class="lead">
    ...
</p>
```

## Task 4: Class utilities for text

### Text: [Bootstrap Docs > Utilities > Text](https://getbootstrap.com/docs/5.3/utilities/text/)

Bootstrap provides standard text utilities to control weight, alignment, and other aspects.

Using [text alignment](https://getbootstrap.com/docs/5.3/utilities/text/#text-alignment) classes, center the  content of the transparency and footer sections:

```html
 <!-- Transparency section -->
<main id="transparency" class="text-center">    
    <h2>...</h2>
    <p>..</p>
</div>

<footer class="text-center">
    ...
</footer>
```

> Text alignment classes also include *text-start* for aligning text to the left and *text-end* for aligning text to the right. 

## Task 5: Class utilities for colors

Reference: [Bootstrap Docs > Utilities > Colors](https://getbootstrap.com/docs/5.3/utilities/colors/)

Color utilities include predefined classes to colorize text. Change the background color to black and the text color to white of the footer's content using the following classes:
- bg-black 
- text-white

```html
<footer class="bg-black text-white">
    &copy; Cafe con Causa 2024. All Rights Reserved.
</footer>
```

Change the background color to *light* of the main section using the class:
- bg-light

```html
<main id="transparency" class="bg-light">
    ...
</main>
```

Bootstrap enables more comprehensive customization when working with colors. We will now use the default [color system](https://getbootstrap.com/docs/5.3/customize/color/). You can also use this system to define [background colors](https://getbootstrap.com/docs/5.3/utilities/background/) of any HTML element.

## Task 6: Class utilities for spacing

Reference: [Bootstrap Docs > Utilities > Spacing](https://getbootstrap.com/docs/5.3/utilities/spacing/)

Spacing utilities provide a [notation](https://getbootstrap.com/docs/5.3/utilities/spacing/#notation) to specify a wide range of shorthand classes related to margin and padding. These shorthand classes follow the syntax {property}{sides}-{size} to set specific values of margin and padding.

Add a gap between the transparency and header sections by adjusting the top margin of the main element used to include the transparency section:

```html
<main class="mt-5">
    ...
</main>
```

Note that *mt-5* follows the notation {property}{sides}-{size} where
- {property} is *m* (margin)
- {sides} is *t* (vertical)
- {size} is *5*

Adjust the margin of the footer section.

```html
<footer class="bg-black text-white text-center py-5">
    &copy; Cafe con Causa 2024. All Rights Reserved.
</footer>
```

## Task 7: Implement a responsive layout

[Bootstrap's grid system](https://getbootstrap.com/docs/5.3/layout/grid/) allows you to arrange content in columns and rows following a  responsive design. The grid layout uses a twelve-column system, which means the width of a single column can vary from one to twelve.

When arranging your content in columns using Bootstrap's grid system, you need to use a combination of *col* classes wrapped inside a *row* class. Add the following structure to the header section:

```html
<div class="container">
    <div class="row">
        <div class="col">
            ...
        </div>
        <div class="col">
            ...
        </div>
    </div>
</div>
```

Furthermore, you can add breakpoints to create a grid system that starts out stacked and becomes horizontal at a given breakpoint. Use the *col-lg* class to display the content of the website as two columns for large screens (*lg* breakpoint) and as one column for smaller screens:

```html
<div class="col-lg">...</div>
```

You may also notice that Bootstrap automatically calculates the size of each column. Specify the number of template columns to adjust the width of each column:

```html
<div class="container">
    <div class="row">
        <div class="col-lg-9">
            ...
        </div>
        <div class="col-lg-3">
            ...
        </div>
    </div>
</div>
```

Using the code above, implement a responsive layout following the layout of the [page's mockup design](https://drive.google.com/file/d/1R7fQwVBQPnJ3DMpoc4sUJmozKeDux1HM/view?usp=sharing)
