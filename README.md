# bidi-sass
Helper SASS mixins for bidirectional websites

## How to install
Just include this file in your sass bundle and you will have access to many easy-to-use bidirectional functions.

## Requirements
You must put the dir="ltr" or dir="rtl" attribute on a parent element. the HTML tag or BODY tag are probably the safest. For example, if you are showing the website in English, use dir="ltr". If you are showing the website in arabic, then you would probably want dir="rtl".

## How to use it
Margin would be a prime candidate for this. Where you would normally have:
```
.some-class {
  margin-left: 10px;
}
```

You would now have:
```
.some-class {
  @include bidi-margin-left(10px);
}
```

This will put the margin on the left for english sites, and on the right for arabic sites.

If you need margins on both sides, you can do this:
```
.some-class {
  @include bidi-margin(0, 25px, 5px, 10px);
}
```

This will always have 0 margin on top and 5px on the bottom. But depending on the language, the left and right margins will swap.

## What next
Read through the file to see what's available. I add as I encounter new cases. Please, create PRs if you have suggestions for additions.
So far it supports:
- margins
- position left and right
- border-radius
- paddings
- translates
- skews
- floats
- text-aligns
- background-positions
- borders
- border-widths

## Bootstrap and other CSS Frameworks
In private projects I have applied this to make bootstrap column layout bidirectional. I can start including files for things like this if there is a demand, although it is quite simple to do.
