#CSS
My resets and preferences

##CSS Resets
Resets: By Michael Bates

___

This is basically set up to override any of Chrome's default handling. Although the idea of CSS resets is not my own; the versions on the web have little in common with mine. Essentially, there is nothing here specifically intended to support older browsers. This is strictly written for the current version of the Chrome browser. Unfortunately Chrome still has some -webkit crap, which requires some prefixing. This is why there are prefixed properties in the resets (buttons). As I continue styling items; this will grow. My intension is to see every "user agent stylesheet" style crossed off in dev tools. This way, I know that all styles are those I've specifically chosen. Hence my resets bare little resemblence to other resets.

___

About the [Universal (*) Selector](#credits-for-inspiring-me): I've read it can slow down a webpage... I don't care. It does what I need; its a tool that I like.

Features:
  1. `/* border: 1px solid rgba(0, 255, 50, 0.9)!important; */`
    1. I keep this commented out, but can be toggled on and off
    2. Easily get a visual reference to elements in my page. It's a handy tool for me.
  2. `box-sizing: border-box;`
    1. This just ensures everything on the page is following this box model.
      1. I only use this box model (no need to mix and match.. doesn't make sense to me; --My Opinion)
      2. Declare it once; now ot doesn't need to be re-declared for any element, class or id... This is the most concise way as far as I know to set this.  This doesn't need to be overridden in cascading styles.
      3. references @CSS Tricks:<sup>1</sup>
    2. this is the box model that makes sense to me and I'm used to styling with this
      1. margin is the only property that does not get coutnted in the size of the box
        1. margin is essentially how your 'box' is spaced relative to other elements('boxes')
        2. then the sizing of the box will take the dimensions you provide in the style properties
      2. `border-box` may be default for most browsers, but I declare it in my resets so that spacing is handled unambiguously.
  3. `position: relative;`
    1. Apparently this can break IE6 -very cool!
    2. Setting everything to relative by default
      1. You can position child elements with absolute positioning (lots of nifty tricks with absolute positioning)
      2. Static, fixed and absolute positioning must be explicitly declared.  Since these are the exceptions -at least in my experience, this makes sense to make the default relative positioning.
  4. `padding: 0; margin: 0;`
    - just my final defaults to remove any browser explicit settings.
    - I don't want margins/ or padding without explicit declarations.

##CSS Preferences
Keeping CSS simple is a never-ending task.  Classes are great, especially when they can be effectively reused.  Styling by id has great specificity, but this can also end up generating hundreds of lines of fairly redundant CSS.

My principles: if you don't use it; don't have it in your style sheet.  Then you don't have far to look when something is not working the way you want.  Using libraries like bootstrap, ionic and the like are recipes for nightmares in styling if you want anything other than their defaults.  It is faster, if you want to customize something, to write your own.  These libraries can be nice references, but use them as references, then write your own.  This way you know what is in your page.

######An aside:
When I was using libraries for default CSS styling, it was uncannily difficult to debug.  In "dev tools", styles might be overriden 20+ times.  Here is a rule of thumb: if you have to use "`!important`" in every class in order to get your style to work, that's a good sign that you should ditch the library you're using and just rewrite into your own css the parts you need, in the style you need.  It will save you many headaches.

On the other hand (if you meet these conditions):
  1. if you're new,
  2. this doesn't overwhelm you,
  3. you have time to sort through overriding styles,

Using these libraries can force you to learn selectors and style properties.  It's a frustrating way to learn, but it might be your kind of learning style.  I learned this way.  I can't say it was the most expedient way to learn, but it definately made me learn.

___
###Using My Preferences
Feel free.  These are here for me to keep my defaults updated.  I don't suspect they will be exceptionally helpful to anyone, but they are by no means private.  Perhaps they may inspire your styles.  But know that these files are not complete stylesheets for any website.  These are just the starters I use when I create a new project.  It's my boilerplate so I'm not rewriting the smae thing over and over.

###Salutations
Cheers and happy Web Developing:
-Mike

___

######Credits for inspiring me:<sup>

<sup>[Things It Might Be Fun/Useful to Try the Universal (*) Selector On](https://css-tricks.com/things-it-might-be-funuseful-to-try-the-universal-selector-on/)</sup>
<sup>I read this article more than a year ago, but it was when I was jsut starting out and it was a tremendous help.  I new use the Universal (*) Selector as noted above.  Thanks Chris for your inspiration.</sup>

___
######References

<sup>1. [**The CSS Box Model**, Chris Coyier](https://css-tricks.com/the-css-box-model/),  [**Box Sizing**, Marie Mosley](https://css-tricks.com/box-sizing/),  [**box-sizing**, Sara Cope](https://css-tricks.com/almanac/properties/b/box-sizing/)</sup>
