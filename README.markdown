## Adam's border-radius Sass mixin
This is a simple mixin (written in SCSS syntax) for the border-radius css3 properties (with webkit, khtml, mozilla and straight-ahead css3 flavors).

## Goals
I've seen border-radius mixins that don't do enough, try to do too much, or are unnecessarily complicated. This is an attempt to write a mixin that is "just right." The goals:

* Handle typical cases, rather than all cases
* Only have one mixin to call
* Compact, flexible and understandable code
* Accomodates using shorthand similar to regular css without having to name variables as you pass values
* Accomodates extra shortcuts by passing named variables with the mixin if you want to

## Not Covered
About the only thing you can't do is make stretched corners, where the horizontal and vertical values for one corner are different. CSS3 lets you do this, but this mixin doesn't. I've never wanted this effect, and can't really picture why anyone would. So, that's left out by design, not by accident. 

## Usage Examples
* <code>.basic-rounded { @include border-radius(10px); }</code>
* <code>.top-rounded { @include border-radius($top:10px); }</code>
* <code>.bottom-rounded { @include border-radius($bottom:10px); }</code>
* <code>.left-rounded { @include border-radius($left:10px); }</code>
* <code>.right-rounded { @include border-radius($right:10px); }</code>
* <code>.top-left-rounded { @include border-radius($top-left:10px); }</code>
* <code>.bottom-right-rounded { @include border-radius($bottom-right:10px); }</code>
* <code>.goofy-rounding { @include border-radius($top-right:5px, $bottom-right:8px, $bottom-left:5px); }</code>
* <code>.goofy-rounding-alt { @include border-radius(0 5px 8px); }</code>