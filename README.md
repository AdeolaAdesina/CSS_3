# CSS_3 Introduction to the Box Model

Browsers load HTML elements with default position values. 

This often leads to an unexpected and unwanted user experience while limiting the views you can create. 

In this lesson, you will learn about the box model, an important concept to understand how elements are positioned and displayed on a website.

All elements on a web page are interpreted by the browser as “living” inside of a box. This is what is meant by the box model.

For example, when you change the background color of an element, you change the background color of its entire box.

In this lesson, you’ll learn about the following aspects of the box model:

- The dimensions of an element’s box.
- The borders of an element’s box.
- The paddings of an element’s box.
- The margins of an element’s box.


## Class work

Take some time to explore the code to the right. See if you can figure out how these following CSS properties impact how an element is displayed:

- width
- height
- padding
- border
- margin
- overflow

```
body {
  background-color: white;
  font-family: 'Raleway', sans-serif;
}

.navigation ul {
  margin: 0;
  padding: 0;
  text-align: center;
}

.navigation li {
  font-weight: 100;
  letter-spacing: 2px;
  padding: 20px;
}

.navigation  li.logo {
  color: black;
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 4px;
}

#banner {
  background-image: url("https://content.codecademy.com/courses/web-101/unit-6/htmlcss1-img_tahoe.jpeg");
  background-size: cover;
  background-position: bottom center;
  height: 700px;
  width: 100%;
}

#banner .content h1 {
  border: 3px solid white;
  position: relative;
  top: 50px;
  width: 400px;
  margin: 0 auto;
}

#main {
  margin: 0 auto;
  padding: 40px;
  text-align: center;
  width: 400px;
  height: 1000px;
  overflow: scroll;
}

h1 {
  color: white;
  font-size: 42px;
  font-weight: 600;
  text-align: center;
}

h2 {
  border: 1px dotted red;
  color: red;
  font-size: 14px;
  line-height: 48px;
  padding: 20px 30px;
  margin: 30px 20px;
  text-align: center;
}

h3 {
  color: red;
  font-size: 26px;
  font-weight: 700;
  padding: 20px 10px;
}

p {
  color: grey;
  font-size: 16px;
  line-height: 48px;
  margin-top: 60px;
  padding: 10px 20px;
}

.pull-quote {
  margin: 0 auto;
  width: 400px;
}

.byline {
  border-bottom: 1px solid LightGrey;
  border-top: 1px solid LightGrey;
  color: DarkGrey;
  font-size: 14px;
  font-weight: 200;
}

.share {
  border: 1px solid LightGrey;
  padding: 40px 0px;
  position: relative;
  text-align: center;
  width: 100%;
}

.share a {
  background: red;
  border: 1px solid red;
  border-radius: 3px;
  color: white;
  display: inline-block;
  margin: 10px;
  padding: 14px;
  text-decoration: none;
}

.share a:hover {
  background: white;
  border: 1px solid red;
  color: red;
}
```


# The Box Model

The box model comprises the set of properties that define parts of an element that take up space on a web page. 

The model includes the content area’s size (width and height) and the element’s padding, border, and margin. The properties include:


- width and height: The width and height of the content area.
- padding: The amount of space between the content area and the border.
- border: The thickness and style of the border surrounding the content area and padding.
- margin: The amount of space between the border and the outside edge of the element.


# Height and Width

An element’s content has two dimensions: a height and a width. By default, the dimensions of an HTML box are set to hold the raw contents of the box.

The CSS height and width properties can be used to modify these default dimensions.

```
p {
  height: 80px;
  width: 240px;
}
```

# Class work

Here's the index.txt and style.css file for this class:

index.txt:

```
<!DOCTYPE html>
<html>
<head>
  <title>The Terminal - Your Source for Fact-Based News</title>
  <link href="https://fonts.googleapis.com/css?family=Amatic+SC|Raleway:100,200,600,700" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <nav class="navigation">
    <ul>
      <li>LOCAL</li>
      <li>NATIONAL</li>
      <li class="logo">THE TERMINAL</li>
      <li>GLOBAL</li>
      <li>OPED</li>
      <li class="donate">DONATE</li>
    </ul>
  </nav>

  <div id="banner">
    <div class="content">
      <h1>Conservation Efforts at Lake Tahoe Being Praised by Nation's Leaders</h1>
    </div>
  </div>

  <div id="main" class="content">
    <h3>THE STATE'S LATEST CONSERVATION EFFORTS ARE BEING HERALDED BY NATION'S TOP LEADERS AS GROUNDBREAKING AND FORWARD THINKING.</h3>
    <span class="byline">WRITTEN BY: JAMES JAYCE</span>
    <p>Until recently, construction on the banks of the Lake had been largely under the control of real estate developers. Construction activities have resulted in a clouding of the lake's blue waters. Currently, the Tahoe Regional Planning Agency is regulating construction along the shoreline and has won two Federal Supreme Court battles over recent decisions. These regulations are unpopular with many residents, especially those in the Tahoe Lakefront Homeowners Association.</p>

    <p>The League to Save Lake Tahoe (Keep Tahoe Blue) has been an environmental watchdog in the Lake Tahoe Basin for 50 years. Founded when a proposal to build a four-lane highway around the lake (with a bridge over the entrance to Emerald Bay) was proposed in 1957, the League has thwarted poorly designed development projects and environmentally unsound planning. The League embraces responsible and diversified use of the Lake's resources while protecting and restoring its natural attributes.</p>

    <div class="pull-quote">
      <h2>"THE LEAGUE EMBRACES RESPONSIBLE AND DIVERSIFIED USE OF THE LAKE'S RESOURCES WHILE PROTECTING AND RESTORING ITS NATURAL ATTRIBUTES"</h2>
    </div>

    <p>Since 1980, the Lake Tahoe Interagency Monitoring Program (LTIMP) has been measuring stream discharge and concentrations of nutrients and sediment in up to 10 tributary streams in the Lake Tahoe Basin, California-Nevada. The objectives of the LTIMP are to acquire and disseminate the water quality information necessary to support science-based environmental planning and decision making in the basin. The LTIMP is a cooperative program with support from 12 federal and state agencies with interests in the Tahoe Basin. This data set, together with more recently acquired data on urban runoff water quality, is being used by the Lahontan Regional Water Quality Control Board to develop a program (mandated by the Clean Water Act) to limit the flux of nutrients and fine sediment to the Lake.</p>

    <p>UC Davis remains a primary steward of the lake. The UC Davis Tahoe Environmental Research Center is dedicated to research, education and public outreach, and to providing objective scientific information for restoration and sustainable use of the Lake Tahoe Basin. Each year, it produces a well-publicized "State of the Lake" assessment report.</p>
  </div>

  <div class="share">
    <a href="#">SHARE</a>
    <a href="#">FAVORITE</a>
    <a href="#">READ</a>
  </div>

</body>
</html>
```


style.css:

```
body {
  background-color: white;
  font-family: 'Raleway', sans-serif;
}

.navigation ul {
  margin: 0;
  padding: 0;
  text-align: center;
}

.navigation li {
  font-weight: 100;
  letter-spacing: 2px;
}

.navigation  li.logo {
  color: black;
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 4px;
}

#banner {
  background-image: url("https://content.codecademy.com/courses/web-101/unit-6/htmlcss1-img_tahoe.jpeg");
  background-size: cover;
  background-position: bottom center;
  width: 100%;
}

#banner .content h1 {
  position: relative;
  top: 50px;
  margin: 0 auto;
}

#main {
  padding: 40px;
  text-align: center;
  width: 400px;
}

h1 {
  color: white;
  font-size: 42px;
  font-weight: 600;
  text-align: center;
}

h2 {
  color: red;
  font-size: 14px;
  line-height: 48px;
  text-align: center;
}

h3 {
  color: red;
  font-size: 26px;
  font-weight: 700;
  padding: 20px 10px;
}

p {
  color: grey;
  font-size: 16px;
  line-height: 48px;
}

.pull-quote {
}

.byline {
  border-bottom: 1px solid LightGrey;
  border-top: 1px solid LightGrey;
  color: DarkGrey;
  font-size: 14px;
  font-weight: 200;
}

.share {
  border: 1px solid LightGrey;
  padding: 40px 0px;
  position: relative;
  text-align: center;
  width: 100%;
}

.share a {
  background: red;
  border: 1px solid red;
  border-radius: 3px;
  color: white;
  display: inline-block;
  text-decoration: none;
}

.share a:hover {
  background: white;
  border: 1px solid red;
  color: red;
}
```


1. Add a height of 700 pixels to #banner.

2 Set .pull-quote width to 350 pixels.

3 Set the #banner .content h1 width to 400 pixels.
