# Starwars opening crawl, in CSS3 and HTML5

## Basically
A bit of fun doing the famous crawling text of Starwars. Nothing really major here, it uses transforms and animations from CSS3. I used Lea Verou's Prefixfree script (many thanks!) so I don't have to care about vendor prefixes (it is especially a pain with animations and keyframes). Audio is basic HTML5 with JS API

## Demos
Demos here: http://tanguymartin.com/demos/starwars-opening/

## More about it
* The audio is preloaded with JavaScript and then when the browser is ready to play it, the animation starts. This prevent the animation to not be in sync with the audio.
* I use "visibility: hidden" to hide the main "STARWARS" title at the begining. I originally used "opacity:0" and then put it back to the value 1 in the animation keyframe 0, but there is a bug in Chrome at the moment of writing whereby scaling transformations don't work when opacity is used.
* The main Starwars title is a SVG image I've taken somewhere (I don't remember where, I'll put the link here when I remember). There was a black background originally so I modified it to be transparent.
* As I said above, the Prefixfree script from Lea Verrou is used to take care of all the prefixing (most usefull for transformations, animations and keyframes)
* Modernizr is used to detect if the browser supports 3D transforms, audio and javascript.

## Where it should work (Tested working on)
* Firefox 15, OSX
* Safari & Chrome, OSX
* ...to be completed

## Where it doesn't work
* On Firefox 14 and below, the crawling text is flickering. There is a workaround but I prefer to leave it as it is for now at least.
* On Opera 12.01, the perspective is not applied to the crawling text. And it doesn't scroll at all.
* On browser that don't support at all either the html5 audio or the css3 transforms/animations

## Resources used
* MDN Documentation on CSS animations: https://developer.mozilla.org/en-US/docs/CSS/CSS_animations
* About the starwars opening crawl: http://www.theforce.net/fanfilms/postproduction/crawl/opening.asp
* http://modernizr.com/
* http://leaverou.github.com/prefixfree/
* ...more to come when I remember

Feel free to report bugs or do pull requests if you judge it is necessary