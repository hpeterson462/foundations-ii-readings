# Videos

## *Styling HTML5 Forms*

* Basic Styles:
    * body
        * background
        * margin
        * font-family
    * header
        * background
        * padding
        * text-align
    * form
        * margin
        * color
    * form p
        * font-size
        * letter-spacing
* Radio Box Styles:
    * input[type="radio"]
        * opacity
        * width
        * margin
        
    * label[for="male"], label[for="female"]
        * margin
        * padding
        * display: inline-block
        * background: url(img/checked.png) no-repeat;
        * background-position: 0 -32px;
        * line-height
        * cursor
    * input: checked + label[for='male']
    * input: checked + label[for='female']
        * (when adjacent to male/female is checked => style)
        * background-position: 0 0;
        * color
    * input[type='checkbox']
        * opacity
        * width
        * margin
    * label[for="web"], label[for="photoshop"], label[for="madona"]
        * display: inline-block;
        * margin
        * padding 
        * background: url(img/checked.png)no-repeat;
        * background-position: 0 -98px;
        * line-height
        * cursor
    * input:checked + label[for="web"], input:checked + label[for="photoshop"], input:checked + label[for="madona"]
        * background-position: 0 -65px;
        * color
* Text Input & Fieldset Styles:
    * fieldset
        * padding
        * margin
        * border
    * legend
        * padding
        * font-size
        * letter-spacing
    * input[type="email"], input[type="telephone"]
        * display: block;
        * margin
        * padding
        * border
        * border-radius
        * background: url(img/input.png)no-repeat;
        * background-color
        * font-size
        * color
        * float: left
    * input[type="email"]
        * background-position
    * input[type="telephone"]
        * background-position
* Select Box Styles:
    * select
        * -webkit-appearance: none;
        * -moz-appearance: none;
        * -ms-appearance: none;
        * -o-appearance: none;
        * appearance: none;
        * display: block;
        * margin
        * padding
        * background: url(img/select.png)no-repeat 95% center;
            * (no-repeat (aligns horizontal) (aligns vertical))
        * background-color
        * color
        * border-radius
        * border
        * width
    * input[type="telephone"]
        * background
        * padding
        * color
        * font-size
        * letter-spacing
        * border-radius
        * border
        * box-shadow: 1px 3px 5px rbga(0, 0, 0, 5);
        * width
* Input Validation Styles
    * input[type="email"]:valid, input[type="telephone"]:valid
        * border
    * input[type="email"]:valid
        * background-position
    * input[type="telephone"]:valid
        * background-position
    * input[type="email"]:valid + .tick, input[type="telephone"]:valid + .tick
        * background: url(img/tick.png)
        * background-size
        * width
        * height
        * float: left:left;
        * margin
    

