---
title: How to build and host a simple website
tags:
 - design
 - beginner
sitemap: true
articleidx: 1
---

Building a simple website isn't very hard. In this article we will build a
simple one page website with a decent looking design.


## Designing the website
We'll design a simple website with a navigation bar, a big fat header a 3 column
aside and then a list of features with screenshots.

![Screenshot](/images/final-screenshot.png)
####You can see how it looks here: [final demo](/raw/htdaw/bg.html)

### CSS Frameworks
Before we start punching in code, let's take a look at the CSS frameworks
available. There are many grid based and responsive CSS frameworks available
today, these make it very easy to build a website with minimum effort. Some of
these are:

  1. [ Bootstrap ](http://getbootstrap.com/)
  2. [Foundation](http://foundation.zurb.com/)
  3. [PureCSS](http://purecss.io/)
  4. [Skeleton](http://www.getskeleton.com/)

We'll use Bootstrap as it is the most popular, and easy to learn.

### Including the stylesheets and javascript files
Bootstrap's css and javascript files are available on maxcdn, you can use these
instead of downloading them and serving them from your own server.

~~~~html
<link href='//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css' />
<script src='//code.jquery.com/jquery-2.1.1.min.js' />
<script src='//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js' />
~~~~

Our HTML

~~~~html
<!doctype HTML><!-- to declare an html5 document -->
<html lang="en">
  <head>

    <!-- meta stuff -->
    <meta charset="utf-8"/>
    <meta content="An awesome navigation demo page." name="description"/>
    <meta content="Khaja Minhajuddin" name="author"/>
    <link rel="canonical" href="http://docs.websrvr.in/raw/htdaw/nav.html"/>
    <title>Our awesome navigation page</title>

    <!-- to stop mobile browsers from lying-->
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- it is a good idea to have a sitemap with all your site's links-->
    <link rel="sitemap" type="application/xml" title="Sitemap" href="/sitemap.xml"/>

    <!-- our bootstrap includes -->
    <link href='//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/css/bootstrap.min.css' rel='stylesheet' type='text/css' />

    <!-- html5 shiv for IE to allow for using of html5 tags in IE browsers whose
       version is less than 9 -->
    <!--[if lt IE 9]
    <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
    -->

    <!-- always good to have a favicon -->
    <link href="/favicon.ico" rel="shortcut icon" />

  </head>
  <body class='nav'>

    <!-- centers and constrains the inner div to 1200 px on medium screens -->
    <!-- almost all of it is documented on the bootstrap documentation
         http://getbootstrap.com/-->
    <div class="container">
      <div class="header">
        <ul class="nav nav-pills pull-right">
          <li class="active"><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
        <h3 class="text-muted">Awesome Navigation</h3>
      </div>
    </div>

    <!-- bootstrap js depends on jQuery-->
    <script src='//code.jquery.com/jquery-2.1.1.min.js'></script>
    <script src='//maxcdn.bootstrapcdn.com/bootstrap/3.2.0/js/bootstrap.min.js'></script>
  </body>
</html>
~~~~

####You can see how it looks here: [navigation demo](/raw/htdaw/nav.html)

###Fat header
You can use bootstrap's jumbotron class to get a nice header and tagline.

~~~~html
<style type="text/css">
  .jumbotron-container{
    margin-top: 20px;
  }
</style>
<div class="container jumbotron-container text-center">
  <div class="jumbotron">
    <h1>Buy my awesome doodahs!</h1>
    <p class="lead">
      These are the best doodahs you'll ever use.
    </p>
    <a href="#" class='btn btn-lg btn-success'>Buy them now</a>
  </div>
</div>
~~~~
####You can see how it looks here: [header demo](/raw/htdaw/header.html)

###Asides
We'll use bootstrap's 12 column grid to get 3 columns

~~~~html
<div class="container asides">
  <div class="row">
    <div class="col-md-4">
      <div class='thumbnail'>
        <img src='http://showcase.websrvr.in/images/screenshots/www.websrvr.in.png' />
        <div class="caption text-center">
          <h3>Awesome feature 1</h3>
          <p>
            Here is some description of the awesome features of our product.
            Phooey kablooey.
            <br />
            <a href="#" class="btn btn-primary" role="button">View More</a>
          </p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class='thumbnail'>
        <img src='http://showcase.websrvr.in/images/screenshots/www.websrvr.in.png' />
        <div class="caption text-center">
          <h3>Awesome feature 2</h3>
          <p>
            Here is some description of the awesome features of our product.
            Phooey kablooey.
            <br />
            <a href="#" class="btn btn-primary" role="button">View More</a>
          </p>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class='thumbnail'>
        <img src='http://showcase.websrvr.in/images/screenshots/www.websrvr.in.png' />
        <div class="caption text-center">
          <h3>Awesome feature 3</h3>
          <p>
            Here is some description of the awesome features of our product.
            Phooey kablooey.
            <br />
            <a href="#" class="btn btn-primary" role="button">View More</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</div>
~~~~
####You can see how it looks here: [asides demo](/raw/htdaw/asides.html)


###Features list
We'll use 2/3rds of the row for text and 1/3rd for the image.

~~~~html
<div class="container features">
  <div class="row feature-row">
    <div class="col-md-8">
      <h3>First featurette heading. It'll blow your mind.</h3>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
    </div>
    <div class="col-md-4">
      <img src="/images/lap1.jpg" alt="placeholder" class='img-responsive' />
    </div>
  </div>
  <div class="row feature-row">
    <div class="col-md-4">
      <img src="/images/lap1.jpg" alt="placeholder" class='img-responsive' />
    </div>
    <div class="col-md-8">
      <h3>First featurette heading. It'll blow your mind.</h3>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
    </div>
  </div>
  <div class="row feature-row">
    <div class="col-md-8">
      <h3>First featurette heading. It'll blow your mind.</h3>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
      <p class='lead'>
        Donec ullamcorper nulla non metus auctor fringilla. Vestibulum id ligula porta felis euismod semper. Praesent commodo cursus magna,
        vel scelerisque nisl consectetur. Fusce dapibus, tellus ac cursus commodo.
      </p>
    </div>
    <div class="col-md-4">
      <img src="/images/lap1.jpg" alt="placeholder" class='img-responsive' />
    </div>
  </div>
</div>
~~~~
####You can see how it looks here: [features demo](/raw/htdaw/features.html)

###Footer
Now, we'll add a simple footer

~~~~html
<div class="container footer-container">
  <div class="footer">
    <p class="text-muted text-center">
      &copy; 2014 Foo bar Inc. All lefts reserved.
    </p>
  </div>
</div>
~~~~
####You can see how it looks here: [footer demo](/raw/htdaw/footer.html)

###Fonts
We can spice this up using free fonts from google web fonts.

~~~~html
@import url("http://fonts.googleapis.com/css?family=Oswald:400,300|Open+Sans:400,600");
~~~~
####You can see how it looks here: [fonts demo](/raw/htdaw/fonts.html)

###Background to make it pop
We can add a good background to make it look a bit more interesting.

~~~~html
body{
  background: url('http://getsimplepage.s3.amazonaws.com/images/cover/58.jpg') no-repeat center center fixed;
  -moz-background-size: cover;
  -webkit-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}
.wrapper{
  background-color: rgba(0, 0, 0, 0.7);
}
~~~~
####You can see how it looks here: [background demo](/raw/htdaw/bg.html)
