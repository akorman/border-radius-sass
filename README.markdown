## Adam's border-radius Sass mixin
This is a simple mixin (written in SCSS syntax) for the border-radius css3 properties (with webkit, khtml, mozilla and straight-ahead css3 flavors).

## Goals
I've seen border-radius mixins that don't do enough (e.g., just handle rounding all corners to the same value) or too much (address all the capabilities of CSS3, even if you ). This is an attempt to write a mixin that is "just right."

If you just want to borrow from Compass (rather than use the whole thing), it's almost impossible to decipher. Also, it's my understanding that vendor prefixes for -ms and -o aren't necessary for border-radius, so I've left them out.
* Handle typical cases, rather than all cases
* You only need to remember one mixin to call
* Compact, flexible and understandable code
* Accomodates using shorthand similar to regular css without having to name variables as you pass values
* Accomodates extra shortcuts by passing named variables with the mixin

What's not covered? Stretched corners, where the horizontal and vertical values for one corner are different. CSS3 lets you do this, but this mixin doesn't. That's by design, not by accident. 

## Usage Examples
* .basic-rounded { @include border-radius(10px); }
* .top-rounded { @include border-radius($top:10px); }
* .bottom-rounded { @include border-radius($bottom:10px); }
* .left-rounded { @include border-radius($left:10px); }
* .right-rounded { @include border-radius($right:10px); }
* .top-left-rounded { @include border-radius($top-left:10px); }
* .bottom-right-rounded { @include border-radius($bottom-right:10px); }
* .goofy-rounding { @include border-radius($top-right:5px, $bottom-right:8px, $bottom-left:5px); }
* .goofy-rounding-alt { @include border-radius(0 5px 8px); }