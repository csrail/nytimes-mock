##Exploration
A static mock website of the *Space Ripples Reveal Big Bang’s Smoking Gun* article from [nytimes.com](http://www.nytimes.com/2014/03/18/science/space/detection-of-waves-in-space-buttresses-landmark-theory-of-big-bang.html?_r=1)

Check out my [version](https://rawgit.com/csrail/nytimes-mock/master/article.html).

##Exposition
This project is backed by a reinforced understanding of CSS principles:
- box model
- floats
- positioning

##Excursions
Rendering a button is serious work! The best way I have found is to include both an image and a span surrounding text inside.
- Position the image using `top`, `right`, `left` and `bottom`; note that this is not the same as `margin-top`, `margin-right`, `margin-left` or `margin-bottom`! Adjusting the margins leads to both the image and the text within the button to move and this is not desirably - we only want the image co-ordinates to move around.
- Set padding to `0` to see how the button renders around the image and text then adjust the position of the image, then add padding as required to plump up the button.
- Set the background-color of the button to anything desirable and the button instantly turns into a coloured div! This is exactly what we want for semantics.

It seems that any margins or paddings applied to a list element causes all list elements to move alongside. I believe this rule is to keep all list elements flush with one another. I have not been able to keep the options icon under the ul class `user--access-acount` as I needed to level it out but could not get around disentangling this flush mechanic. I have instead opted - hopefully there is a better solution - to extract out the item from the list as a button on its own, wrap it in a div and float it to the right. This means that the button had to be moved higher up the html document which decreases flow and the readability. This is because my workflow is to read items from left to right on the webpage therefore my html document should also read from top to bottom with no "jumping" around which is occurring here.