# Tutorial: Bootstrap Basics
In this tutorial, we will use the front-end development framework [Bootstrap](https://getbootstrap.com/), one of the most popular frameworks for styling websites. 

In this tutorial, each task contains links to [Bootstrap official documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/). The purpose of this tutorial is to let you familiarize yourself with Bootstrap's documentation and apply Bootstrap's predefined CSS classes to style your website.

### Download the resources

We will work with a design inspired by the [New Age](https://startbootstrap.com/previews/new-age) template from the [Start Bootstrap](https://startbootstrap.com/) website.

Download the base code from [here](https://github.com/josecarlosgt/bootstrap/raw/tutorial-basics/base.zip). We will work with the **index.html** file and the images included in the assets directory.

[Link to the page narrative](https://docs.google.com/document/d/1tnplJskdtc41upRjyfd3wu_NzxDQAH3-NoEJXKJdbco/edit?usp=sharing)

Link to the mockup designs:
- [Main page](https://drive.google.com/file/d/1R7fQwVBQPnJ3DMpoc4sUJmozKeDux1HM/view?usp=sharing)
- [Main page with modal window](https://drive.google.com/file/d/1iaGfRBPpbkQHqXAf56o62qmWy_FzNQh8/view?usp=sharing)

## Task 1: Page's settings and introduction

Let's first specify the page's title and meta description:

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

Bootstrap also provides several features for styling text content that allows you to create customized headings, paragraphs, and lists.

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

> Text alignment classes also include *text-start* for aligning text to the left and *text-end* for aligning text to the right. 

## Task 5: Class utilities for colors

Reference: [Bootstrap Docs > Utilities > Colors](https://getbootstrap.com/docs/5.3/utilities/colors/)

Color utilities include predefined classes to colorize text. Change the background color to black and the text color to white of the footer's content using the following classes:
- bg-black 
- text-white

Change the background color to *light* of the FAQ section using the class:
- bg-light

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

Add a gap between the transparency and header sections by adjusting the top margin of the main element used to include the transparency section:

Adjust the margin and padding of the FAQ and footer sections.

## Task 7: Adding icons
Reference: https://icons.getbootstrap.com/

Finally, try out the Bootstrap Icons library to add icons to your webpage. To use the Bootstrap icons library, you need to add the corresponding CSS resource into the \<head\> tag:

```html
<link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.0/font/bootstrap-icons.css" rel="stylesheet">
```

Add a chat icon preceding the *Contact Us* phrase on the navigation menu:

```html
<i class="bi-chat-text-fill me-2"></i>
```

## Content Panels

## Task 8: [Slider](https://getbootstrap.com/docs/5.3/components/carousel/)

A slider positions a series of images next to each other but only shows one at a time. The images then slide from one to the next. In Bootstrap, the slider is called the carousel.

The following slider provides buttons that allow users to navigate between each of the slides:

```html
<!-- Slider -->
<div id="carousel-coffee" class="carousel slide" data-bs-ride="carousel">
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
    <button class="carousel-control-prev" type="button" data-bs-target="#carousel-coffee"
        data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carousel-coffee"
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

## Task 9: [Accordion](https://getbootstrap.com/docs/5.3/components/accordion/)

The accordion comprises a collection of content organized as pairs of titles and panels. When you click on the title of an accordion, its corresponding panel expands to reveal the content.

```html
<!-- accordion -->
<div class="accordion" id="faq-content">
    <article class="accordion-item">
        <h2 class="accordion-header" id="heading-1">
            <button class="accordion-button fw-bold" type="button" data-bs-toggle="collapse"
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
            <button class="accordion-button collapsed fw-bold" type="button" data-bs-toggle="collapse"
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
## Task 10: [Modal Window](https://getbootstrap.com/docs/5.3/components/modal/)

Also known as pop-up, the modal window is content that appears "in front of" the rest of the page's content.

We will create a "Contact Us" [form](https://getbootstrap.com/docs/5.0/forms/overview/
) as a modal using the Bootstrap modal component.

The template provided to you already contains, as part of the navigation bar, the button to trigger the modal window:

```html
<button class="btn btn-primary rounded-pill px-3 mb-2 mb-lg-0" data-bs-toggle="modal"
    data-bs-target="#feedbackModal">
    <span class="d-flex align-items-center">
        <i class="bi-chat-text-fill me-2"></i>
        <span class="small">Contact Us</span>
    </span>
</button>
```

The content for the modal window will typically sit within the page, but it is hidden when the page loads using CSS. Add the modal content at the bottom of the page:

```html
<div class="modal fade" id="feedbackModal" tabindex="-1" aria-labelledby="feedbackModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
            <div class="modal-header bg-gradient-primary-to-secondary p-4">
                <h5 class="modal-title" id="feedbackModalLabel">Contact Us</h5>
                <button class="btn-close" type="button" data-bs-dismiss="modal"
                    aria-label="Close"></button>
            </div>
            <div class="modal-body border-0 p-4">
                <form>
                    <div class="form-group mb-4">
                        <label for="email" class="form-label">Email address:</label>
                        <input type="email" class="form-control" id="email" placeholder="Enter your email">
                    </div>
                    <div class="form-group mb-4">
                        <label for="name" class="form-label">Name:</label>
                        <input type="text" class="form-control" id="name" placeholder="Enter your name">
                    </div>
                    <div class="form-group mb-4">
                        <label for="comment" class="form-label">Comment:</label>
                        <textarea class="form-control" id="comment" rows="3"></textarea>
                    </div>
                    <div class="text-center">
                        <button class="btn btn-secondary rounded-pill btn-lg disabled w-100" id="submitButton" type="submit">Submit</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>
```

## Other Content Panels

Bootstrap also has available several other components to implement content panels:
- [Offcanvas](https://getbootstrap.com/docs/5.3/components/offcanvas/)
- [Dropdowns](https://getbootstrap.com/docs/5.3/components/dropdowns/)
- [Tabs](https://getbootstrap.com/docs/5.3/components/navs-tabs/)