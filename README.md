# Teaching - AProfessionalNetwork.com

Here you can find the instructions on how to build a single page webpage based on html/css, created for anyone who'd like to start coding, but would not know where to start. There will be some links included to help you out, some code examples and remember, all code can also be found in the repository itself. See however how far you can get with just this read me first!

<hr>

## Set Up

* Open up your text editor and create a new folder:  
      'website'
* Create a new file:
      'about-me.html'
* Create the type, head & body of the file:
```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>All about {your name}!</title>
  </head>

  <body>
  </body>
</html>

```


## Structure
* Divide the body into four sections. Give them names, like this:

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>All about {your name}!</title>
  </head>

  <body>
    <section class="header">
    </section>

    <section class="banner">
    </section>

    <section class="info">
    </section>

    <section class="footer">
    </section>
  </body>
</html>
```
  Don't forget to 'indent'! By placing the elements inside the body two spaces to the right, we can easily see what's part of   the body and what's not. (There is some discussion about the ideal layout of HTML, you can find more info on [Granneman](https://www.granneman.com/webdev/coding/formatting-and-indenting-your-html/) and [w3 schools](https://www.w3schools.com/html/html5_syntax.asp).)

* Add an h1 with the web address inside the header section (more info on tags can be found [here](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started), a list of tags you can use can be found [here](https://www.w3schools.com/tags/ref_byfunc.asp).)
```
  <body>
    <header class= "header">
      <h1>AProfessionalNetwork.com</h1>
    </header>
```

* Add an image to the ‘banner-section’. Add an h5 with your name and an h6 with a catchy subtitle:
```
    <section class="banner">
      <img src="https://cdn-media-1.lifehack.org/wp-content/files/2017/07/28041858/UzfYe5hQRu2jKDd3voqC_full_boring.001.jpeg" alt="Me />
      <h1>MyName</h1>
      <h3>Write your catchy subtitle here!</h3>
    </section>
```

* Add an h2 to the ‘info-section’  with the (sub)title: ‘Work’

* Add several divs with information to your ‘info-section’. A div might look like this:

```
<div >
  <h5>Developer/Codaisseur</h5>
  <h6> 2017 - now <h6>
  <p> Jodilodileedilodielodieleedilodilee jadiladilodileidejodilaordiejeoplido! Topijopieropeicopiesopeinopielopielei, padiemadie, sadiejiora jakfojaiowignkaldfjaiwojfvivei! </p>
  <hr>
</div>
```

* If you have some time left, repeat the last two steps, but now call this section education. Or hobbies. Or favorite food.     Whatever you like!



## Styling

* We'll be styling our page with [CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/How_CSS_works). To keep the file from becoming chaotic, we'll write our code in a separate file. In your website directory, create a new file stylesheet.css

* To link our html and css files together, we'll need to add one line of code to our head section in our html page:

```
  <head>
    <meta charset="utf-8">
    <title>All about Mimi!</title>
    <link rel='stylesheet' href='./stylesheet.css'
  </head>
```

* Now we can start styling our page! First we will work on the text. This example will work for all html inside the body:
```
body {
  font-family: Verdana, sans-serif;
  font-size: 25px;
  line-height: 1.5;
  margin: 0;
}
```
  We could later overwrite it by calling out the elements seperately:
```
h5 {
  color: #353535;
  font-size: 20px;
  margin: 10px 0;
}
```
  [Here](https://www.w3schools.com/css/css_text.asp) you can find an overview with all sorts of text formatting properties.

* We can also style the sections, by calling their names like this:

```
.header {
  padding: 5px;
  font-size: 15px;
  background-color: #009688;
  border-bottom: 2px;
  border-color: #fff;
  margin-top: 0px;
  width: 100%;
  position: fixed;
}
```
  DON'T FORGET THE DOT! Sections (usually called boxes) can be styled in many different ways, some of which can be found [here](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_boxes). But seriously, googling helps. Everything has been done before, so the code you want will be online somewhere!

Just try out what you like, take a look at the code in this repository, or at one of the templates [here](https://www.w3schools.com/w3css/w3css_templates.asp).

And that's it! Now we have a beautiful page for our fictive website!

<hr>

## BONUS: Links

In this part we will be creating a navbar!

* First of all, remove your h1 from the header section and replace it with with an unordered list:
```
<section class= "header">
  <ul>
  </ul>
</section>
```

* Now, add four empty list items to your unordered list:

```
<section class= "header">
  <ul>
    <li> </li>
    <li> </li>
    <li> </li>
    <li> </li>
  </ul>
</section>
```

* Add a [link](https://www.w3schools.com/html/html_links.asp) to each list item. A link will look like this:

```
<a href="path/to/your/file">what the user will see</a>
```
 In our case, our list might look like this:
```
<section class= "header">
  <ul>
    <li><a href="./info.html" class="website">AProfessionalNetwork.com</a></li>
    <li><a href="./bio.thml">Bio</a></li>
    <li><a href="./calendar.html">Calendar</a></li>
    <li><a href="./contact.html">Contact</a></li>
  </ul>
</section>
```
Now we have four clickable links! At the moment, they won't lead to any page, yet, but you could create more pages by adding and bio.html, calendar.html and a contact.html file to your ' website' directory!

It still looks ugly though. Let's style it a bit more:


* In your sylesheet.css file, write the following code. What do you think it will do?
```
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}
```

* Now style the list elements (li) to display next to each other, rarther than vertically:

```
li {
  display: inline;
}
```

* And we will add some styling for the links itself, how they look normally, what they look like when you hover over them and what they look like when you click on them:

```
a {
  float: left;
  color: #000;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

a:hover {
    background-color: #ddd;
    color: black;
}

a:active {
    background-color: #4CAF50;
    color: white;
}
```
Cool, looks way better! Would you know a way to make the website name stand out a little more? And if you are really really fast or continuing at home, create the bio, calendar and contact page!

<hr>

(full powerpoint of the accompanying lectures with this class can be found [here](https://docs.google.com/presentation/d/1JWfMkMNB2b6p8A7rPkn6j4ijKcdOYdJeDoytPijJe8I/edit?usp=sharing)
 )
