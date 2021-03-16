# Notes taken while watching [this](https://www.youtube.com/watch?v=yfoY53QXEnI&t=619s&ab_channel=TraversyMedia) css tutorial on youtube
- css selectors:
  a {background-color : yellow; }
    - a : selector ( can be html tag, or id, or class)
    - background-color : property
    - yello : value
- including a css file in html page.  
  - &lt;link rel="stylesheet" type="text/css" href="<rel-path> or ... ">
- colors in css
  - color names : red, coral,
  - html5 color names : 
  - hexadecimal : #00ff00
  - rgb : rgb(0, 0, 255)
  
- fonts   
  - websafe fonts ( I think standard fonts are websafe fonts, see what it really means)
  - font-family
    - Ariel, Helvetica, ... 
- id vs class
  - `id` is really unique
  - use `class` to apply reusable styles
  - `bootstrap` doesn't use the id
- a selector for class starts with a `dot` (.)
- \* : all the tags, define at the top
    ```css
      *{
        margin : 10px
        color : red
      }
    ```


- box model. 
    - <img src="/assets/box-model-css.png" width="250" height="250" />
- target tags within a class
  ```css
  .box-1 h1{
  }
  ```
  This will only target `h1` within the `box-1` class.
  
- href="#" : Use inside `a` tag to go nowhere
- Apply some css to a specific tag within a class
  - ```css
    .categories h1{
    }
    /*
    Applied to the h1 within a class categories
    */
    ```
- css for different states of `link` tag
  - ```css
    a:hover{
      /*
      When you hover over a link
      */
    }
    a:active{
    /*
      Right after you click on a link
    */
    }
    a:visited{
      /*
        After you click on a link
      */
    }
    ```
- css for id
  - ```css
    #class-name{
    }
    ```
- css properties
  - background-color
  - color
  - font-family
  - font-size : 16px
  - font-weight : boldness
  - font: normal 16px Ariel, Helvetica, sans-serif (specify multiple font properties at the same time)
  - line-height : 1.6em (can control the spacing between the lines)
  - margin: 
    - auto :  set same margin on both side (left and right)
  - width (to contain the content of the website within a box of specified size
    - don't set to pixels to make the content responsive
    - use 80%
  - margin-top, margin-bottom, margin-left, margin-right
  - margin : 5px 10px 5px 10px (top, clockwise), 5px 10px (top/bottom, left/right)
  - padding : same as margin
  - border-right : 5px red solid
  - border-left :
  - border-top:
  - border-bottom: 
  - border:
  - border-bottom-width : 10px
  - border-top-style : dotted
  - text-decoration: (underline, ...)
  - text-transform : (uppercase, ...)
  - letter-spacing : 0.2em 
  - word-spacing : 1em
  - border-radius : curved box for text box
  - list-style : bullet style in lists
  - list-style-image: url()
  - float: (left, ...) arrange text-boxes horizontally
  - box-sizing: border-box (play around with the horizontal width of text boxes (flexbox takes care of these things)j
