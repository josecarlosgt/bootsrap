# Tutorial: Customizing a Bootstrap Template

This tutorial consists of customizing a Bootstrap template. You will practice your skills on:

- Choosing and elaborating on the topic for a webpage
- Creating content for a webpage
- Customizing an existing template

## Instructions

Think of a place that you have enjoyed visiting in your life. The site you chose will serve as the topic of your webpage.

Then, think of three stories that illustrate the place you chose. These stories will serve as the content of your webpage. Although each story is different, all of them should relate to your webpage's topic, making your webpage distinct while maintaining the focus of your webpage on a single idea. Selecting and elaborating on a topic makes it easier to concretize a message on our web pages and create content, such as images and text, to communicate the message.

After deciding on a place and three related stories, complete the following tasks.

## Task 0: Get the template

We will use the [One Page Wonder](https://startbootstrap.com/theme/one-page-wonder) template from the [Start Bootstrap](https://startbootstrap.com/) website. Download the template from [here](https://github.com/josecarlosgt/bootsrap/blob/tutorial-templates-landmark/landmark-template.zip?raw=true).

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

## Task 4: Customize the stories

Update each section's Lorem ipsum placeholder text by writing one or two statements that describe your stories. Each story should also have a title displayed as an h2 heading element.

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

> Try to obtain images of about of size 700 x 700 px. Also, all your pictures should be of the same size.

## Task 5: Customize the general description

Customize the About section at the end of the webpage. You can include any text that complements the content in your stories. For example, you may add a general description of the place or say something about its location, such as the country or local culture. 

Add a [slider](https://getbootstrap.com/docs/5.0/components/carousel/) with controls with three images. The images can also be of size 700 x 700 px. All your images should be of the same size. Your pictures should be related to the content in this section.

## Task 6: Update the navigation bar

Customize the navigation bar so that the text in each link describes each story. Also, add a link for the About section. 

## Task 7: Publish your webpage on GitHub Pages

Finally, create a repository for your webpage on GitHub and publish it on GitHub Pages.
