# Introduction #

Math equations was supported since about v0.65 to v0.7 of original Wiki2touch by preparing a collection of images for each and every of the latex math equations, however, due to the versatile and ever-increasing nature of the contents, pre-rendered images may not fit forever.

In recent years, browsers have gained marvelous advancements, with improvements of javascript being an important one among them. JSMath is a project utilizing javascipt technologies to display LaTeX maths in Web pages. (http://www.math.union.edu/~dpvc/jsMath/welcome.html)

By incorporating JSMath into Wiki2touch Server, which is a mini web server, most Wikipedia math could be supported without generating and packing extra image files.

# Usage #

Some patches to the math content handling code in both WikiMarkupParser class, HTML template and style sheets has been committed to the branches codes, enabling the JSMath functionality.

To toggle-on this feature, just run the daemon with an extra argument '-jsmath'. Or in other word, add an extra line of argument `<string>`-jsmath`</string>` into the array of 'ProgramArguments' of the plist **/System/Library/LaunchDaemons/com.wiki.wikisrvd.plist**.

In the browser, when a math equation is shown, the math environment should be labeled with green color, and a hint in red afterward. To show the result of a particular equation, just click on it. After rendering, the result will replace the original LaTeX content. (NOTE: first click in a page may be slow due to the loading of scripts.)

# Tuning the JSMath #

JSMath saves its settings in browser's cookies. To adjust the options, click 'jsmath' button after it is loaded and drawn in the lower right corner when you scroll to the top of the page (in MobileSafari only, and for other browsers, the position is fixed at lower right corner).

# Troubleshooting #

Set JSMath options to 'Use native Unicode fonts'.