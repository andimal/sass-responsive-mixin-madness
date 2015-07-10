#Sass Responsive Mixin Madness

[HTML5 Chicago Lightning Talks 7/9/15](http://www.meetup.com/chicago-html5/events/222482831/)

Supercharge your responsive workflow with Sass mixins.

---

Install & Run:
```
git clone git@github.com:andimal/sass-responsive-mixin-madness.git
cd /path/to/directory
bundle install
middleman
```

The important bits:
```
// variables
$screen-sm      : 480px
$screen-md      : 768px
$screen-lg      : 1200px

// mixins
=media-xs
  +media(max-width $screen-sm - 1) // this mixin comes from Bourbon Neat, btw
    @content

=media-sm
  +media(min-width $screen-sm)
    @content

=media-md
  +media(min-width $screen-md)
    @content

=media-lg
  +media(min-width $screen-lg)
    @content

// use the mixins inside your elements!
.responsive-container
  width: 400px
  height: 400px
  background-color: red

  +media-sm
    background-color: blue

  +media-md
    background-color: green
```
