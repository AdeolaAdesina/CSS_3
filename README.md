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


style.css:

```
#banner {
  background-image: url("https://content.codecademy.com/courses/web-101/unit-6/htmlcss1-img_tahoe.jpeg");
  background-size: cover;
  background-position: bottom center;
  width: 100%;
  height: 700px;
}

#banner .content h1 {
  position: relative;
  top: 50px;
  margin: 0 auto;
  height: 700px;
  width: 400px;
}

.pull-quote {
  width: 350px;
}
```



# Borders

A border is a line that surrounds an element, like a frame around a painting. 

Borders can be set with a specific width, style, and color:

- width—The thickness of the border. A border’s thickness can be set in pixels or with one of the following keywords: THIN, MEDIUM, or THICK.
- style—The design of the border. Web browsers can render any of 10 different styles. Some of these styles include: NONE, DOTTED, and SOLID.
- color—The color of the border. Web browsers can render colors using a few different formats, including 140 built-in color keywords.


```
p {
  border: 3px solid coral;
}
```

In the example above, the border has a width of 3 pixels, a style of solid, and a color of coral. All three properties are set in one line of code.

The default border is medium none color, where color is the current color of the element. 

If width, style, or color are not set in the CSS file, the web browser assigns the default value for that property.

```
p.content-header {
  height: 80px;
  width: 240px;
  border: solid coral;
}
```

In this example, the border style is set to solid and the color is set to coral. The width is not set, so it defaults to medium.

## Class work

1 Add a dotted red border with 1-pixel thickness to all h2 headings.

2 Add a solid, white border, with a 3 pixel width, to the #banner .content h1 rule.

style.css:

```
h2 {
  color: red;
  font-size: 14px;
  line-height: 48px;
  text-align: center;
  border: 1px dotted red;
}

#banner .content h1 {
  position: relative;
  top: 50px;
  width: 400px;
  margin: 0 auto;
  border: 3px solid white;
}
```

# Border Radius

Ever since we revealed the borders of boxes, you may have noticed that the borders highlight the true shape of an element’s box: square. 

Thanks to CSS, a border doesn’t have to be square.

You can modify the corners of an element’s border box with the border-radius property.

```
div.container {
  border: 3px solid blue;
  border-radius: 5px;
}
```

The code in the example above will set all four corners of the border to a radius of 5 pixels (i.e. the same curvature that a circle with a radius of 5 pixels would have).

You can create a border that is a perfect circle by first creating an element with the same width and height, and then setting the radius equal to half the width of the box, which is 50%.

```div.container {
  height: 60px;
  width: 60px;
  border: 3px solid blue;
  border-radius: 50%;
}
```

## Class work

In style.css, set the border radius of #banner .content h1 to 15 pixels.

Additionally, try experimenting with other border-radius values and running your code to see the result!

style.css:

```
#banner .content h1 {
  border: solid 3px white;
  position: relative;
  top: 50px;
  width: 400px;
  margin: 0 auto;
  border-radius: 15px;
}
```


# Padding

The space between the contents of a box and the borders of a box is known as padding. 

Padding is like the space between a picture and the frame surrounding it. 

In CSS, you can modify this space with the padding property.

```
p.content-header {
  border: 3px solid coral;
  padding: 10px;
}
```

The code in this example puts 10 pixels of space between the content of the paragraph (the text) and the borders, on all four sides.

If you want to be more specific about the amount of padding on each side of a box’s content, you can use the following properties:

- padding-top
- padding-right
- padding-bottom
- padding-left

```
p.content-header {
  border: 3px solid fuchsia;
  padding-bottom: 10px;
}
```

In the example above, only the bottom side of the paragraph’s content will have a padding of 10 pixels.


## Class work

1 In a single line, set the .navigation li elements to have 20 pixels of padding.

2 Look at the red boxes at the bottom of the web page. Set the .share a elements to have 14 pixels of padding in style.css and run your code.

3 Set the top and bottom padding of h2 elements to 20 pixels and set the left and right padding of h2 elements to 30 pixels.

style.css:

```
.navigation li {
  font-weight: 100;
  letter-spacing: 2px;
  padding: 20px;
}

.share a {
  background: red;
  border: 1px solid red;
  border-radius: 3px;
  color: white;
  display: inline-block;
  text-decoration: none;
  padding: 14px;
}

h2 {
  border: 1px dotted red;
  color: red;
  font-size: 14px;
  line-height: 48px;
  text-align: center;
  padding-top: 20px;
  padding-bottom: 20px;
  padding-right: 30px;
  padding-left: 30px;
}
```



# Padding Shorthand

Another implementation of the padding property lets you specify exactly how much padding there should be on each side of the content in a single declaration. 

A declaration that uses multiple properties as values is known as a shorthand property.


Padding shorthand lets you specify all of the padding properties as values on a single line:

- padding-top
- padding-right
- padding-bottom
- padding-left

You can specify these properties in a few different ways:

## 4 Values

```
p.content-header {
  padding: 6px 11px 4px 9px;
}
```

In order, it specifies the padding-top value (6px), the padding-right value (11px), the padding-bottom value (4px), and the padding-left value (9px) of the content.


## 3 Values

```
p.content-header {
  padding: 5px 10px 20px;
}
```

The first value sets the padding-top value (5px), the second value sets the padding-left and padding-right values (10px), and the third value sets the padding-bottom value (20px).


## 2 Values

```
p.content-header {
  padding: 5px 10px;
}
```

The first value sets the padding-top and padding-bottom values (5px), and the second value sets the padding-left and padding-right values (10px).


## Class work

1 Change the individual padding declarations on the h2 selector ruleset to use padding shorthand with 2 values. Keep the padding for the top and bottom at 20 pixels and the value for the left and right padding at 30 pixels.

2. Using two values for the padding property, set the padding of the p element to 10 pixels on the top and bottom and 20 pixels on the left and right.

style.css:

```
h2 {
  border: 1px dotted red;
  color: red;
  font-size: 14px;
  line-height: 48px;
  text-align: center;
  padding: 20px 30px;
}

p {
  color: grey;
  font-size: 16px;
  line-height: 48px;
  padding: 10px 20px;
}
```


# Margin

So far you’ve learned about the following components of the box model: content, borders, and padding. The fourth and final component of the box model is margin.

Margin refers to the space directly outside of the box. The margin property is used to specify the size of this space.

```
p {
  border: 1px solid aquamarine;
  margin: 20px;
}
```

The code in the example above will place 20 pixels of space on the outside of the paragraph’s box on all four sides.

If you want to be even more specific about the amount of margin on each side of a box, you can use the following properties:

- margin-top
- margin-right
- margin-bottom
- margin-left

Each property affects the margin on only one side of the box, providing more flexibility in customization.

```
p {
  border: 3px solid DarkSlateGrey;
  margin-right: 15px;
}
```


## Class work

1 Set the top margin of p elements to 60 pixels.

2 Look at the three red boxes at the bottom of the web page. These elements are anchor elements of class .share. Set these .share a elements to have a margin of 10 pixels.

style.css:

```
p {
  color: grey;
  font-size: 16px;
  line-height: 48px;
  padding: 10px 20px;
  margin-top: 60px;
}

.share a {
  background: red;
  border: 1px solid red;
  border-radius: 3px;
  color: white;
  display: inline-block;
  padding: 14px;
  text-decoration: none;
  margin: 10px;
}
```


# Margin Shorthand

The shorthand syntax for margins is the same as padding, so if you’re feeling comfortable with that, skip to the instructions. 

Otherwise, read on to learn how to use margin shorthand!

Similar to padding shorthand, margin shorthand lets you specify all of the margin properties as values on a single line:

- margin-top
- margin-right
- margin-bottom
- margin-left


You can specify these properties in a few different ways:

## 4 Values

```
p {
  margin: 6px 10px 5px 12px;
}
```

it specifies the margin-top value (6px), the margin-right value (10px), the margin-bottom value (5px), and the margin-left value (12px) of the content.

## 3 Values

```
p {
  margin: 5px 12px 4px;
}
```

The first value sets the margin-top value (5px), the second value sets the margin-left and margin-right values (12px), and the third value sets the margin-bottom value (4px).


## 2 Values

```
p {
  margin: 20px 10px;
}
```

The first value sets the margin-top and margin-bottom values (20px), and the second value sets the margin-left and margin-right values (10px).


## Class work

Using two values, set the h2 top and bottom margins to 30 pixels and the left and right margins to 20 pixels.


style.css:

```
h2 {
  border: 1px dotted red;
  color: red;
  font-size: 14px;
  line-height: 48px;
  padding: 20px 30px;
  text-align: center;
  margin: 30px 20px;
}
```

# Auto

The margin property also lets you center content. However, you must follow a few syntax requirements. Take a look at the following example:

```
div.headline {
  width: 400px;
  margin: 0 auto;
}
```

In the example above, margin: 0 auto; will center the divs in their containing elements. 

The 0 sets the top and bottom margins to 0 pixels. 

The auto value instructs the browser to adjust the left and right margins until the element is centered within its containing element.

In order to center an element, a width must be set for that element. Otherwise, the width of the div will be automatically set to the full width of its containing element, like the <body>, for example.

In the example above, the width of the div is set to 400 pixels, which is less than the width of most screens. This will cause the div to center within a containing element that is greater than 400 pixels wide.

## Class work

1 Set the width of the .pull-quote class elements to 350 pixels.

2 In one line, set the vertical (top and bottom) margins of the .pull-quote class to 0 and the horizontal (left and right) margins to auto.

3 Set the vertical margins of the #main element to 0, and the horizontal margins to auto.

style.css:

```
.pull-quote {
  width: 350px;
}

.pull-quote {
  width: 350px;
  margin: 0 auto;
}

#main {
  padding: 40px;
  text-align: center;
  width: 400px;
  margin: 0 auto;
}
```


# Margin Collapse

As you have seen, padding is space added inside an element’s border, while margin is space added outside an element’s border. One additional difference is that top and bottom margins, also called vertical margins, collapse, while top and bottom padding does not.

Horizontal margins (left and right), like padding, are always displayed and added together. 

For example, if two divs with ids #div-one and #div-two, are next to each other, they will be as far apart as the sum of their adjacent margins.

```
#img-one {
  margin-right: 20px;
}
 
#img-two {
  margin-left: 20px;
}
```

In this example, the space between the #img-one and #img-two borders is 40 pixels. 

The right margin of #img-one (20px) and the left margin of #img-two (20px) add to make a total margin of 40 pixels.

Unlike horizontal margins, vertical margins do not add. Instead, the larger of the two vertical margins sets the distance between adjacent elements.

```
#img-one {
  margin-bottom: 30px;
}
 
#img-two {
  margin-top: 20px;
}
```

In this example, the vertical margin between the #img-one and #img-two elements is 30 pixels. Although the sum of the margins is 50 pixels, the margin collapses so the spacing is only dependent on the #img-one bottom margin.

![Screenshot_140](https://user-images.githubusercontent.com/29931071/200281089-37355e20-d422-4d31-ae2b-779a7c961076.png)


# Minimum and Maximum Height and Width

Because a web page can be viewed through displays of differing screen size, the content on the web page can suffer from those changes in size. 

To avoid this problem, CSS offers two properties that can limit how narrow or how wide an element’s box can be sized to:

- min-width—this property ensures a minimum width of an element’s box.
- max-width—this property ensures a maximum width of an element’s box.


```
p {
  min-width: 300px;
  max-width: 600px;
}
```

In the example above, the width of all paragraphs will not shrink below 300 pixels, nor will the width exceed 600 pixels.

You can also limit the minimum and maximum height of an element:

- min-height — this property ensures a minimum height for an element’s box.
- max-height — this property ensures a maximum height of an element’s box.

```
p {
  min-height: 150px;
  max-height: 300px;
}
```

In the example above, the height of all paragraphs will not shrink below 150 pixels and the height will not exceed 300 pixels.


## Class work

1 In style.css, set the minimum width of the p element to 200 pixels.

After you’ve done this successfully, resize the browser and notice how the paragraph’s box will no longer shrink below 200 pixels.

2 Next, set the maximum width of the p element to 800 pixels.

After you’ve done this successfully, resize the browser and notice how the paragraph’s box will no longer expand beyond 800 pixels.

3 In style.css, set the minimum height of the p element to 200 pixels.

After you’ve done this successfully, resize the browser and notice how the height of paragraph’s box will no longer shrink below 200 pixels.

4 In style.css, set the maximum height of the p element to 300 pixels.

After you’ve done this successfully, resize the browser and notice how the height of paragraph’s box will no longer expand beyond 300 pixels. You should see your text overflowing. In the next exercise, we will fix that!


# Overflow

How can we ensure that we can view all of an element that is larger than its parent’s containing area?

The overflow property controls what happens to content that spills, or overflows, outside its box. The most commonly used values are:

- hidden—when set to this value, any content that overflows will be hidden from view.
- scroll—when set to this value, a scrollbar will be added to the element’s box so that the rest of the content can be viewed by scrolling.
- visible—when set to this value, the overflow content will be displayed outside of the containing element. Note, this is the default value.

```
p {
  overflow: scroll; 
}
```

In the example above, if any of the paragraph content overflows (perhaps a user resizes their browser window), a scrollbar will appear so that users can view the rest of the content.

The overflow property is set on a parent element to instruct a web browser on how to render child elements. For example, if a div’s overflow property is set to scroll, all children of this div will display overflowing content with a scroll bar.


## Class work

1 In order to see the impact of overflow: scroll, first change the height of the #main element to 1000 pixels.

2 Set the overflow of the #main element to scroll.

When you scroll down, a second scroll bar should appear over the paragraph section. You may have to expand the browser component in order to see this behavior clearly.


style.css:

```
#main {
  margin: 0 auto;
  padding: 40px;
  text-align: center;
  width: 400px;
  height: 1000px;
  overflow: scroll;
}
```

