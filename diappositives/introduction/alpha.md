!SLIDE subsection
# introduction #

!SLIDE bullets
.notes something

# Second Slide #

* something
* something else
* a third thing
* a fourth thing
* a fifth thing

!SLIDE bullets
# Third Slide

* Sometimes bullet items
  * Have sublists
  * And some sublist items
    * Have some of their own
    * And so on
* But top-level "bullet items" have no bullets
  * isn't that odd?

Also, sometimes you just want to have plain text sitting in the middle
of the screen. The quick brown fox jumps over the lazy dog.

!SLIDE center
.notes another dark side

![octocat](octocat.png)

!SLIDE
.notes notes for my slide

	@@@ javascript
	function setupPreso() {
	  if (preso_started)
	  {
	     alert("already started")
	     return
	  }
	  preso_started = true

	  loadSlides()
	  doDebugStuff()

	  document.onkeydown = keyDown
	}

!SLIDE commandline

	$ git commit -am 'incremental bullet points working'
	[master ac5fd8a] incremental bullet points working
	 2 files changed, 32 insertions(+), 5 deletions(-)
