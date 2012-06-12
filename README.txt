** LICENSE **

Released under the Apache License 2.0.
http://www.apache.org/licenses/LICENSE-2.0.html


** SUMMARY **
Guiders (Speech Overlay) are a user experience design pattern for introducing users to a web application.  Check out README.html for Guiders (Speech Overlay) in action!


** INITIALIZING Guiders (Speech Overlay) **
Here is sample code for initializing a couple of Guiders (Speech Overlay).  Guiders (Speech Overlay) are hidden when created, unless .show() is method chained immediately after .createGuider.

guider.createGuider({
  buttons: [{name: "Next"}],
  description: "Guiders (Speech Overlay) are a user interface design pattern for introducing features of software. This dialog box, for example, is the first in a series of Guiders (Speech Overlay) that together make up a guide.",
  id: "first",
  next: "second",
  overlay: true,
  title: "Welcome to Guiders.js!"
}).show();
/* .show() means that this guider will get shown immediately after creation. */
           
guider.createGuider({
  attachTo: "#clock",
  buttons: [{name: "Close, then click on the clock.", onclick: guider.hideAll}],
  description: "Custom event handlers can be used to hide and show Guiders (Speech Overlay). This allows you to interactively show the user how to use your software by having them complete steps. To try it, click on the clock.",
  id: "third",
  next: "fourth",
  position: 2,
  title: "You can also advance Guiders (Speech Overlay) from custom event handlers.",
  width: 450
});

The parameters for creating Guiders (Speech Overlay) are:
attachTo: (optional) selector of the html element you want to attach the guider to
buttons: array of button objects
  {
    name: "Close",
    classString: "primary-button",
    onclick: callback function for when the button is clicked
      (if name is "close" or "next", onclick defaults to guider.hideAll and guider.next respectively)
   }
buttonCustomHTML: (optional) custom HTML that gets appended to the buttons div
description: text description that shows up inside the guider
overlay: (optional) if true, an overlay will pop up between the guider and the rest of the page
position: (optional / required if using attachTo) clock position at which the guider should be attached to the html element
title: title of the guider
width: (optional) custom width of the guider (it defaults to 400px)


** INTEGRATION WITH YOUR WEB APPLICATION **
Besides creating Guiders (Speech Overlay), here is sample code you can use in your application to work with Guiders (Speech Overlay):

guider.hideAll(); // hides all Guiders (Speech Overlay)
guider.next(); // hides the last shown guider, if shown, and advances to the next guider
guider.show(id); // shows the guider, given the id used at creation

You'll likely want to change the default values, such as the width (set to 400px).  These can be found at the top of guider.js in the _defaultSettings object.  You'll also want to modify the css file to match your application's branding.

** IN CLOSING **
Guiders (Speech Overlay) are a great way to improve the user experience of your web application.  If you're interested in optimizing user experience through A/B testing, check out Optimizely (optimizely.com).  We're the people who built Guiders (Speech Overlay) in the first place.
If you have questions about Guiders (Speech Overlay) or Optimizely, email us at jeff+pickhardt@optimizely.com or hello@optimizely.com.
