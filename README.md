# Tutorial: Styling the content of your website with Bootstrap
In this tutorial, we will use a front-end/CSS framework called [Bootstrap](https://getbootstrap.com/), one of the most popular frameworks for styling websites. 

In this tutorial, you will find several links to [Bootstrap official documentation](https://getbootstrap.com/docs/5.3/getting-started/introduction/) in each task. This tutorial's main purpose is to familiarize yourself with the Bootstrap documentation and apply Bootstrap pre-defined CSS classes to style your website.

### Download the resources

We will work with a design inspired in the [New Age](https://startbootstrap.com/previews/new-age) template from the [Start Bootstrap](https://startbootstrap.com/) website. Download the base code from [here](https://github.com/josecarlosgt/bootstrap/raw/tutorial-1-styling/base.zip).

## Task 11: Create a container for the header section

[Bootstrap's grid system](https://getbootstrap.com/docs/5.3/layout/grid/) allows you to arrange content in columns and rows following a fully responsive design. The grid layout uses a twelve-column system which means the width of a single column can vary from one to twelve.

When arranging your content in columns using Bootstrap grid system, you need to use a combination of *col* classes wrapped inside a *row* class. Add the following structure to the header section:

```html
<header>
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
</header>
```

Furthermore, you can add breakpoints to create a grid system that starts out stacked and becomes horizontal at a given breakpoint. Use the *col-lg* class to display the content of the website as two columns for large screens (*lg* breakpoint) and as one column for smaller screens:

```html
<div class="col-lg">...</div>
```

You may also notice that Bootstrap automatically calculates the size of each column. Specify the number of template columns to adjust the width of each column:

```html
<header>
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
</header>
```

## Task 12: Create a container for the FAQs section

Create a container for the FAQs section that for large screens display two columns of equal size:
1. On the first column (start), display the following image:
```html
<img src="assets/img/faq.jpeg" class="img-fluid" alt="Cup of coffee and coffee beans">
```

2. On the second column (end) display the accordion with the FAQs content.

You may also specify [gutters](https://getbootstrap.com/docs/5.3/layout/gutters/) (padding between columns) to keep a gap between the image and accordion when the content stacks into one single column:

```html
<div class="row g-5">...</div>
```

## Task 13: Create a responsive navigation menu

Use the [navbar](https://getbootstrap.com/docs/5.3/components/navbar/) component to add responsive behaviour to the navigation bar at the top:

```html
<nav class="navbar fixed-top navbar-expand-lg navbar-light bg-light">
    <div class="container px-5">
        <a class="navbar-brand fw-bold" href="#page-top">Start</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarResponsive"
            aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
            Menu
            <i class="bi-list"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
            <ul class="navbar-nav ms-auto me-4 my-3 my-lg-0">
                <li class="nav-item"><a class="nav-link me-lg-3" href="#transparency">Transparency</a></li>
                <li class="nav-item"><a class="nav-link me-lg-3" href="#faq">FAQ</a></li>
            </ul>
            <button class="btn btn-primary rounded-pill px-3 mb-2 mb-lg-0" data-bs-toggle="modal"
                data-bs-target="#feedbackModal">
                <span class="d-flex align-items-center">
                    <i class="bi-chat-text-fill me-2"></i>
                    <span class="small">Contact Us</span>
                </span>
            </button>
        </div>
    </div>
</nav>
```

## Task 14: Adjust the layout

Note the navigation bar above uses a *fixed-top* class that allows the user to access the navigation bar anywhere on the page. Carefully revise the appereance of the page and perform any necessary adjustments.

## Task 15: Add a three-column panel using the [Cards](https://getbootstrap.com/docs/5.3/components/card/)

First, create a container for the main (transparency) section:

```html
<main id="transparency" class="pt-5">
    <div class="container">
        <div class="text-center">
            <h2 class="display-5">Transparency</h2>
            <p class="lead">We believe in the importance of being transparent in everything we do by providing you with information on costs, expenses, earnings and impact data.</p>
        </div>
    <div class="row my-4 g-0 justify-content-center">
        <!-- Cards content -->
    </div>
</main>
```

Then, organize the content of the transparency using the Bootstrap cards component. A card acts as a content container that includes options for headers and footers. 

We will use the *article* element to create each card:

```html
<article class="card border-0">
    <img class="card-img-top" src="..." alt="...">
    <div class="card-body">
        <h4 class="card-title text-center">[TRANSPARENCY SUBSECTION]</h4>
        <p class="card-text">
            <p class="mb-2">
                [TRANSPARENCY SUBSECTION DESCRIPTION]
            </p>
        </p>
    </div>
</article>
```

Create three cards with the content of the transparency section.
