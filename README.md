# Customizing a Bootstrap Template

In this laboratory practice, you will explore the Bootstrap framework by customizing a pre-designed template. Bootstrap is a powerful front-end toolkit that simplifies the process of building responsive web pages. By using its built-in classes and components, you can create professional-looking websites with minimal coding effort.

## Instructions

Think of a place that you have enjoyed visiting in your life. The site you chose will serve as the topic of your webpage.

Then, think of two stories that illustrate the place you chose. These stories will serve as the content of your webpage. Although each story is different, all of them should relate to your webpage's topic, making your webpage distinct and maintaining the focus of your webpage on a single idea. Selecting and elaborating on a topic makes it easier to concretize a message on our web pages and create content aligned with the web page's main message.

After deciding on a place and stories, complete the following tasks.

## Task 0: Get the template

We will use the [One Page Wonder](https://startbootstrap.com/theme/one-page-wonder) template from the [Start Bootstrap](https://startbootstrap.com/) website. You can download the original template from the Start Bootstrap or download a pre-customized template from [here](https://github.com/josecarlosgt/bootsrap/blob/tutorial-templates-landmark/landmark-template.zip?raw=true). The pre-customized template will make it easier to complete the following tasks.

## Task 1: Customize the page's settings

Update the webpage head settings.

```html
<title>[PAGE TITLE]</title>
<meta name="description" content="[DESCRIPTION]" />
```

## Task 2: Customize the favicon image

Note that the folder assets contain an image called "favicon.ico" displayed next to the page's title on the browser address bar.

> A favicon (short for favorite icon) is a file containing small icons associated with a particular website or web page. Browsers that support favicon display show the page's favicon in the browser's address bar and next to the page's name in a list of bookmarks.

Visit the website [PGN Repot](https://www.pngrepo.com/) and select an image related to your webpage's topic to be used as a favicon. Use the site [ICO Convert](https://icoconvert.com/) to convert the image in PNG format to a .ico image that you can use as a favicon.

Then, place the .ico image in the assets/ folder and update the link element with the .ico path.

```html
<link rel="icon" type="image/x-icon" href="[IMAGE PATH]" />
```

## Task 3: Customize the header

Customize the webpage with a main heading and introduction (welcome blurb or subheading). These texts should represent the topic you chose. 

```html
<h1 ...>[Main header]</h1>
<h2 ...>[Subheader]</h2>
```

## Task 4: Customize the first story

Update the first section's Lorem ipsum placeholder text by writing one or two statements that describe your first story. your story should also have a title displayed as an h2 heading element.

```html
<div class="p-5">
    <h2 class="display-4">[Story 1]</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quod aliquid, mollitia odio veniam sit iste esse assumenda amet aperiam exercitationem, ea animi blanditiis recusandae! Ratione voluptatum molestiae adipisci, beatae obcaecati.</p>
</div>
```

 Update each story by adding an image of your choice to each story. Remember to update the alt attribute of each image element with a description of your pictures. 

```html
<img ... src="http://placehold.jp/700x700.png" alt="..." /></div>
```

> Try to obtain images of about of size 700 x 700 px. Also, all your pictures should be of the same size. Ensure that you specify the dimensions and alternative text for each image.

## Task 5: Add a second story

Copy, paste, and customize the code for your first story to add a second story. You should crack the HTML code to swap the order of your columns, displaying the story image on the left of the grid and the text content on the right.

## Task 6: Add a slider

A slider positions a series of images next to each other but only shows one at a time. The images then slide from one to the next. In bootstrap, the slider is called carousel.

This slider loads several panels but only shows one at a time:

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
    </div>
</div>
<!-- End of Slider -->
```

Notes:
- The *.active* class needs to be added to one of the slides; otherwise, the carousel will not be visible. 
- Also, use a unique id on the *.carousel* to allow controls (below)
- The *data-bs-ride* attribute controls the autoplay
- The carousel uses the *[d-block](https://getbootstrap.com/docs/4.0/utilities/display/)* and *[w-100](https://getbootstrap.com/docs/4.0/utilities/sizing/)* to ensure on carousel images to prevent browser default image alignment.

Add a slider with at least two images at the end of the webpage with text content to the right of the slider. You can include in your slider any images that complement the content in your stories. For example, you may add a general description of the place or say something about its location, such as the country or local culture.

Notes:
- Use the [carousel component](https://getbootstrap.com/docs/5.3/components/carousel/)
- Use a grid of one row and two columns to display the slider on the left column and the description text on the right.

## Task 7: Update the navigation bar

Customize the navigation bar so that the text in each link describes each story. Also, add a link for the slider section. 

## Task 8: Publish your webpage on GitHub Pages

Finally, create a repository for your webpage on GitHub and publish it on GitHub Pages.
