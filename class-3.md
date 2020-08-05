# Articles

## *Responsive Web Design*

* Web design that works on both computers and mobile devices
* Responsive - react quickly and positively to any change
* Adaptive - easily modified for a new purpose or situation
* 3 main components:
    * Flexible layouts
        * flexible grid capable of dynamically resizing
        * fixed units have too many constraints - eg: px
            * `em`, `width`, `margin`, `padding`
            * viewports width `vw`
            * minimum viewports h/w `vmin`
            * viewports height `vh`
            * mximum viewports h/w `vmax`
    * Media queries
        * specify different styles and targeting for individual browsers and devices
        *  `@media` 
        * `min-width` and `max-width`
        * aspect ratio and device-aspect-ratio
    * Mobile first
        * targets smaller viewports
        * conserves bandwidth
        * majority of Internet consumption will soon be done mobile
        * use media queries for viewports over 420px
* Viewport
    * `device-height` `device-width`
    * Viewport scale


## *All About Floats*

* remain a part of the flow of the web page
* absolute positioning removes element from flow of page
* float: right, left, none, inherit
* able to reflow; absolute position  not able to reflow
* clear property - will not move up adjacent to float, but down past the float
* clear: both, left, right, none
* can affect the parent element by collapsing it
* to fix collapse, clear float after floated elements in conainer, but before close of container
* overflow property on parent element will expand to contain floats
* can use psuedo selector `:after` to clear floats
* pushdown is symptom of element inside a floated item being wider than the float itself - use `overflow: hidden` to correct
* double margin bug - `display: inline` to correct
* 3px jog = floated element is kicked away by 3px - set w/h on affected text
* bottom margin bug - floated parent has floated children, bottom margin on children is ignored by parent - use  bottom padding on parent


## *Don't Overthink Grid*

* block level element is a wide as its parent
* when using columns, `box-sizing: border-box` is helpful
* setting width helps element stay at that width
* apply fixed padding on all sides of column
* gutters to space around columns


## *CSS Floats Explained*

* create alternate flows - left and right
* normal flow element (without float) fill in spaces around floated elements
* clear allows elements to specify where they should align in comparison to floated elements


## *Scalable and Modular Architecture for CSS*

* SMACSS is a style guide
* 5 types of categories:
    1) base
        1) heading, default styles, fonts, and backgrounds
    1) layout
        1) divided into major and minor styles
    1) module
        1) navigation bars, carousels, and widgets
    1) state
        1) augments and overrides all other styles
    1) theme
        1) define color and images that give app a certain look/feel
