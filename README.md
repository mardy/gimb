### GIMB, the gimp-save branch.
GIMB is a branch of the popular image manipulation program
[GIMP](http://www.gimp.org) which features a file saving functionality
similar to what was implemented until GIMP 2.6.

### What is wrong with GIMP 2.8?
While GIMP 2.8 continues to be an excellent application, it drastically
changed the way of dealing with JPEG, PNG, and all other non-XCF files.
[The changes are nicely explained
here](http://libregraphicsworld.org/blog/entry/gimp-2.8-understanding-ui-changes).

Those changes are indeed very sensible for most graphic artists, but as
a photographer I find them extremely annoying. Think of someone editing
a hundred of files in a day, using this workflow:
- Open an image in ufraw, fix the colours and send it directly to GIMP
- In GIMP, do some editing (rotate, clone tool, compose the watermark
layer).
- Once done, flatten the image.
- Close the image window.
- As GIMP prompts you to save it, just replace the extension with "jpg"
and press the "Save" button.

Unfortunately this is only possible with GIMP 2.6 -- **and indeed, with
GIMB**! The same workflow with GIMP 2.8 is:
- Open an image in ufraw, fix the colours and send it directly to GIMP
- In GIMP, do some editing (rotate, clone tool, compose the watermark
layer).
- Once done, flatten the image.
- Close the image window.
- As GIMP prompts you to save it, you can just save it as XCF.
- After swearing, cancel the save dialog, end invoke the "Export" action
from the "File" menu. You can now save your image as JPEG.
- Close the image window.
- As GIMP prompts you to save it, swear again.

### Why make a fork?
The GIMP developers have stated many times already that they don't
intend to revert the changes or even to [add an option to facilitate the
non-XCF
workflow](https://mail.gnome.org/archives/gimp-developer-list/2012-November/msg00093.html),
and recommended to use another application or create a fork. So, here it
is. :-)

I'd rather **call it a "branch" rather than a "fork"**, though. The plan
is to keep a set of patches which provide a good file-saving experience
and rebase it on top of the future GIMP releases.

### Future developments
Given my limited free time, all I can commit to is delivering GIMB with
the save feature as described above. So, as far as I am concerned, GIMB
will always be just a regular GIMP with the save functionality from GIMP
2.6 restored.

However, if some developer is willing to spend more time on it and let
GIMB evolve independently from GIMP, I'd be delighted to pass over the
maintainership of it.

In absence of that, my hope is that GIMB will be short lived and that
GIMP developers realize that many people need an efficient, XCF-free,
way of working with images and make the necessary improvements in the GIMP.

