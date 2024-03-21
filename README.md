# Tutorial: Bootstrap's Grid System
In this tutorial, we will use Bootstrap's grid system to style the content of a webpage. 

### Download the resources

Download the base code from [here](https://github.com/josecarlosgt/bootstrap/raw/tutorial-1-styling/base.zip). We will work with the **index.html** file and the images included in the assets directory.

## Task 1: Create a responsive header

[Bootstrap's grid system](https://getbootstrap.com/docs/5.3/layout/grid/) allows you to arrange content in columns and rows following a fully responsive design. The grid layout uses a twelve-column system which means the width of a single column can vary from one to twelve.

When arranging your content in columns using Bootstrap grid system, you need to use a combination of *col* classes wrapped inside a *row* class. Add the following structure to the header section:

```html
<header>
    ...
    <div class="container">
        <div class="row">
            <div class="col">
                <!-- Tagline -->
                ...
            </div>
            <div class="col">
                <!-- Slider -->
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
    ...
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

## Task 2: Create a responsive main section

Implement a three-column grid for the three subsections of the main (transparency) section:

```html
<main id="transparency" class="... container">
    <!-- Section heading -->
    ...
    <div class="row">
        <!-- Subsection 1 -->
        <article class="col-lg ...">
            ...
        </article>
        <!-- Subsection 2 -->
        <article class="col-lg ...">
            ...
        </article>
        <!-- Subsection 3 -->
        <article class="col-lg ...">
            ...
        </article>
    </div>
</main>
```

You may also specify [gutters](https://getbootstrap.com/docs/5.3/layout/gutters/) (padding between columns) to eliminate the gap between the subsections:

```html
<main id="transparency" class="container ...">
    <!-- Section heading -->
    ...
    <div class="row g-0">
        ...
    </div>
</main>
```

## Task 3: Create a responsive FAQs section

Create a container for the FAQs section that for large screens display two columns of equal size:

```html
<aside id="faq" class="container ...">
    <!-- Section heading -->
    ...
    <div class="row">
        <!-- Section image -->
        <div class="col-lg-6">
            ...
        </div>
        <div class="col-lg-6">
            <!-- Accordion -->
        </div>
    </div>
</aside>
```

Add the [img-fluid](https://getbootstrap.com/docs/5.3/content/images/) class to the section image to make it responsive:

```html
<img src="assets/img/faq.jpeg" class="img-fluid" alt="Cup of coffee and coffee beans">
```
