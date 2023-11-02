# Tutorial: Styling the content of your website with Bootstrap
In this tutorial, we will use a front-end/CSS framework called [Bootstrap](https://getbootstrap.com/), one of the most popular frameworks for styling websites. 
We will use Bootstrap for two reasons:
1. Bootstrap makes it faster to style a webpage
2. Bootstrap allows you to build responsive websites and applications

In this tutorial, you will find several links to [Bootstrap official documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/) in each task. This tutorial's main purpose is to familiarize yourself with the Bootstrap documentation and apply Bootstrap pre-defined CSS classes to style your website.

### Download the resources

We will work with a design inspired in the [New Age](https://startbootstrap.com/previews/new-age) template from the [Start Bootstrap](https://startbootstrap.com/) website. Download the base code from [here](https://github.com/josecarlosgt/bootstrap/raw/tutorial-1-styling/base.zip).

## The business case: Café con Causa (Coffee with a Cause)

Café con Causa (Coffee with a Cause) is a nonprofit organization in Guatemala that commercializes Guatemalan coffee to generate resources that create and sustain educational projects in the country's rural communities. Café con Causa provides a commercial platform that involves small producers who grow and harvest coffee. Café con Causa purchases the coffee at a fair price and commercializes it with Guatemala's individuals and companies. All the profits generated by product sales are donated to community schools in the rural areas to promote education for children and youth.

Café con Causa has been a success in Guatemala. Café con Causa has drawn the attention of dozens of companies in the country, from the smallest to the largest in the country, who believe in the causes promoted by the nonprofit. From the success in Guatemala, the CEO of Café con Causa recognized a growth opportunity in the United States to expand Café con Causa's customer base and take the development of community schools in rural Guatemala to new heights. 

We will take the initiative to promote the expansion of Café con Causa in Guatemala as a context for this tutorial. *We will build a website that emphasizes the causes promoted by Café con Causa and the organization's need to project an honest and open image to its potential customers, given its status as a nonprofit organization.* 

We will use the following text to complete the tasks below:

> ***Page title:*** Café con Causa
>
> ***Welcome blurb:*** We commercialize Guatemalan coffee to generate resources that create and sustain educational projects in the rural communities of the country.
>
> **Transparency (section)**
>
> We believe in the importance of being transparent in everything we do by providing you with information on costs, expenses, earnings and impact data.
>
> **Production costs (subsection)**
>
> Thanks to alliances with our suppliers who believed in the project, we managed to have a production cost of $2.34 per unit.
>
> **Expenses Reloaded (subsection)**
>
> Transportation and administration expenses as well as 17% on tax expenditure represent only $1.49 per each bag of coffee.
>
> **Profits (subsection)** 
> 
> With a sales price of $9.00, we generate a profit of $4.77 per unit, which is entirely invested on educational projects.
>
> **Frequently Asked Questions (section)**
>
> - How much does a pound of coffee cost?
> - How can I make an order?
> - How can I place an order from the United States?

## Part I: Basic Bootstrap 

## Task 1: Installing Bootstrap
Reference: [Bootstrap Docs > Introduction](https://getbootstrap.com/docs/5.3/getting-started/introduction/)

The easiest way to add Bootstrap to your website is using the content delivery network (CDN) servers recommended by Boostrap. Other ways of using Bootstrap require downloading the source files, which allows higher customization.

We will use the CDN resources:
- Include the CSS resource into the \<head\> element
- Include the JavaScript resource right before the closing body tag (</body>)
- You also need to include a [responsive meta tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag) which ensures proper rendering of your webpage on mobile devices. This is necessary because Bootstrap automatically optimizes your code for mobile devices.

Put it all together and your webpage should look like this:
```html
<!doctype html>
<html lang="en">
    <head>
    ...
       
        <!-- Responsive metatag -->    
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- Bootstrap CSS -->
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-T3c6CoIi6uLrA9TneNEoa7RxnatzjcDSCmG1MXxSR1GAsXEV/Dwwykc2MPK8M2HN" crossorigin="anonymous">
    </head>
    <body>
        ...
        <!-- Bootstrap JavaScript -->
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-C6RzsynM9kWDrMNeT87bh95OGNyZPhcTNXj1NW7RuBCsyN/o0jlpcV8Qyq46cDfL" crossorigin="anonymous"></script>
  </body>
</html>       
```

> Learn more about the [integrity \(subresource integrity\)](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) and [crossorigin](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/crossorigin) attributes.

## Task 2: Styling text content

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
> Note the display headings classes use a numbering independent of the HTML heading elements. The display headings classes can be used with any HTML element.

The feature [lead](https://getbootstrap.com/docs/5.3/content/typography/#lead) allows you to make paragraphs stand out. We can use this feature for the first paragraph on our website to make it look slightly bigger and relevant than the rest of the paragraphs.

Apply the *lead* class to the paragraphs in the header and transparency sections:

```html
<p class="lead">
    ...
</p>
```

## Task 3: Styling images content

Reference: [Bootstrap Docs > Content > Images](https://getbootstrap.com/docs/5.3/content/images/)

Images in Bootstrap are made responsive with the *.img-fluid* class. Add this class to the images on website's header and FAQ sections:

```html    
<img src="..." class="img-fluid" ...>
...
```

Notes:
- Adding responsive behavior usually involves adjusting the [max-width](https://www.w3schools.com/cssref/pr_dim_max-width.asp) CSS property of HTML elements. This property defines the maximum width of an element's content and it prevents the element from becoming larger than the value specified by max-width.
- img-fluid maintains a 100% max-width regardless of the size of the screen, so images never become larger than their parent elements (containers). As a result, images are resized to fit the screen.
 
## Task 4: Class utilities for text

### Text: [Bootstrap Docs > Utilities > Text](https://getbootstrap.com/docs/5.3/utilities/text/)

Bootstrap provides common text utilities to control weight, alignment, and other aspects.

Using [font weight](https://getbootstrap.com/docs/5.3/utilities/text/#font-weight-and-italics) classes, control the style of the Start link on the navigation menu:

```html
<a class="fw-bold" href="#page-top">Start</a>
```

Using [text alignment](https://getbootstrap.com/docs/5.3/utilities/text/#text-alignment) classes, center the  content of the transparency and footer sections:

```html
<div class="text-center">
    <h2>...</h2>
    <p>..</p>
</div>

<footer class="text-center">
    ...
</footer>
```
Notes:
- Text alignment classes also include *text-start* for aligning text to the left and *text-end* for aligning text to the right. 

## Task 5: Class utilities for colors

Reference: [Bootstrap Docs > Utilities > Colors](https://getbootstrap.com/docs/5.3/utilities/colors/)

Color utilities include predefined classes to colorize text. Change the background color to black and text color to white of the footer's content using the following classes:
- bg-black 
- text-white

Change the background color to *ligth* of the FAQ section using the class:
- bg-light

Bootstrap enables more comprehensive customization for working with colors. For now, we will use the default [color system](https://getbootstrap.com/docs/5.3/customize/color/). You can also use this system for defining [background colors](https://getbootstrap.com/docs/5.3/utilities/background/) of any HTML element.

## Task 7: Class utilities for spacing

Reference: [Bootstrap Docs > Utilities > Spacing](https://getbootstrap.com/docs/5.3/utilities/spacing/)

Spacing utilities provide a [notation](https://getbootstrap.com/docs/5.3/utilities/spacing/#notation) to specify a wide range of shorthand classes related to margin and padding. These shorthand classes follow the syntax {property}{sides}-{size} to set specific values of margin and padding.

Add a gap between the transaprency and header sections by adjusting the top margin of the main element used to include the transparency section:

```html
<main class="mt-5">
    <h2 class="display-5">...</h2>
    <p>
        ...
    </p>
</main>
```

Note that *mt-5* follows the notation {property}{sides}-{size} where
- {property} is *m* (margin)
- {sides} is *t* (vertical)
- {size} is *5*

Add a gap between the transaprency and header sections by adjusting the top margin of the main element used to include the transparency section:

Adjust the margin and padding of the FAQ and footer sections.

## Task 8: Adding icons
Reference: https://icons.getbootstrap.com/

Finally, try out Bootstrap Icons library for adding icons to your webpage. To use Bootstrap icons library, you need to add the corresponding CSS resource into the \<head\> tag:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.4/font/bootstrap-icons.css">
```

Remember we adjusted the color of the warning statement in the first guided visit option? Add an exclamation icon to increase the attention of the viewer:

```html
<i class="bi-exclamation-triangle"></i>
```
>Icons are also a great way to make your content more accessible for people with color blindness.

Final result:
```html
Cross the four kilometres in a kayak guided by a local guide. <strong class="text-warning fw-bold"><i class="bi-exclamation-triangle"></i> This guided visit is physically demanding, and we recommend it for only those in excellent physical condition.</strong>
```

## Part II: Content Panels

## Task 9: [Slider](https://getbootstrap.com/docs/5.3/components/carousel/)

A slider positions a series of images next to each other but only shows one at a time. The images then slide from one to the next. In bootstrap, the slider is called carousel.

The following slider provides buttons that allow users to navigate between each of the slides:

```html
<!-- Slider -->
<div id="carousel-films" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
        <div class="carousel-item active">
            <img src="assets/img/placeholder.png" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
            <img src="assets/img/placeholder.png" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
            <img src="assets/img/placeholder.png" class="d-block w-100" alt="...">
        </div>
    </div>
    <!-- Slider controls -->
    <button class="carousel-control-prev" type="button" data-bs-target="#carousel-films"
        data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carousel-films"
        data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
    </button> 
    </div>
</div>
<!-- End of Slider -->
```

> Create a slider using the Bootstrap carousel component. Replace the *placeholder.png* and *alt* with your content.

Notes:
- The *.active* class needs to be added to one of the slides; otherwise, the carousel will not be visible. 
- Also, use a unique id on the *.carousel* to allow controls (below)
- The *data-bs-ride* attribute controls the autoplay
- The carousel uses the *[d-block](https://getbootstrap.com/docs/4.0/utilities/display/)* and *[w-100](https://getbootstrap.com/docs/4.0/utilities/sizing/)* to ensure on carousel images to prevent browser default image alignment.

## Task 10: [Accordion](https://getbootstrap.com/docs/5.3/components/accordion/)

The accordion comprises a collection of content organized as pairs of titles and panels. When you click on a title of an accordion, its corresponding panel expands to reveal the content.

```html
<!-- accordion -->
<div class="accordion" id="faq-content">
    <article class="accordion-item">
        <h2 class="accordion-header" id="heading-1">
            <button class="accordion-button" type="button" data-bs-toggle="collapse"
                data-bs-target="#faq-1" aria-expanded="true" aria-controls="faq-1">
                [FAQ 1]
            </button>
        </h2>
        <div id="faq-1" class="accordion-collapse collapse show" aria-labelledby="heading-1"
            data-bs-parent="#faq-content">
            <div class="accordion-body">
                <p>
                    [FAQ CONTENT]  
                </p>
            </div>
        </div>
    </article>
    <article class="accordion-item">
        <h2 class="accordion-header" id="heading-2">
            <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                data-bs-target="#faq-2" aria-expanded="false" aria-controls="faq-2">
                [FAQ 2]
            </button>
        </h2>
        <div id="faq-2" class="accordion-collapse collapse" aria-labelledby="heading-2"
            data-bs-parent="#faq-content">
            <div class="accordion-body">
                <p>
                    [FAQ CONTENT] 
                </p>
            </div>
        </div>
    </article>
</div>
<!-- End of accordion -->
```
