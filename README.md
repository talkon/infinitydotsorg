# infinitydotsorg

Feel free to edit this document. Things that should be done reasonably soon are marked with **TODO**; things we plan to include are marked **PLAN**; things we dream of doing are marked **DREAM**.

## Getting started

* **Setting up a local repository.** Due to how Git works, you need to clone this (online) repository to your computer to edit. The easiest way is to use [GitHub Desktop](https://desktop.github.com).
  * Download it at the link above.
  * Login with your GitHub account, which should have access to this repository.
  * Go to Current Repository &rarr; Add &rarr; Clone Repository and find talkon/infinitydotsorg.
  * Pick a (local) folder to put the repository in. From now on, you can edit your local repository in that folder.
* **Git basics.** These are things you need to do when editing the site:
  * Before starting, **fetch origin** to make sure your local repo is up-to-date.
  * After you finish, **commit** to ensure your edits are recorded, then **push to origin** to push your edits to the online repo.
* **The coding itself.** The site is coded in plain HTML with plain CSS<sup>(might be updated to LESS soon)</sup> for style. Resources for these languages can easily be found online. Google is your best friend.

## Meta

* The website is currently hosted by GitHub Pages, which is FREE and only allows hosting of static websites, and has a soft limit of 1GB storage and 100GB bandwidth. We are not anywhere near these limits, so no worries.
* The published branch is `gh-pages`, not `master`. Generally, work on `master` until you are sure the changes can go online, then merge `master` into `gh-pages` to update the site.
* talkon owns the domain https://infinitydots.org and plans to renew it indefinitely.
* The site was redesigned January 2020. The old site (which has more content, actually) can be reached at https://infinitydots.org/old_2019 but it's partly broken, oops.

## Content

* Unless we have more contributor-hours devoted to the site, my (talkon's) plan is to keep the site minimal. 
* The only real upkeep we need to do is to keep the InfinityDots MO and the Archive pages regularly updated.
* > **TODO**: Create an InfinityDots MO 4 page and keep it updated
* **PLAN**: Port and revive blog if there is enough interest.
* **DREAM**: (Suggested by Tdl) Run a weekly/monthly problems page similar to https://www.aldaily.com but with the columns for easy/medium/hard problems.
* **DREAM**: Keep a database of problems in $\TeX$ with metadata such as contest, year, subject, difficulty, topics used; auto-generate tests/exams/problem sets based on these attributes.

## Design

* `red.css` is the currently used CSS file. `red_old.css`, as its name says, defines the old style before the redesign.
* See current pages (ex. mo.html) for example of divs to be used.
* Design langueage: each page shold have a background color (ex. black), a text color (white), and a tint color (red). Special texts should be somewhere between the text and the tint color.
* > **TODO**: Adjust screen width cutoff; site should be in no-sidebar mode for slightly larger widths
* **PLAN**: Convert the above to LESS, and upgrade the site from CSS to LESS. This allows us to easily change the tint-color, say, for InfinityDots JMO page (blue)
* **DREAM**: Animate the logo on hover using SVG and CSS magic. Ideally the red (or whatever the tint color is) dots should rotate under the white infinity sign.

## Tips

* To include code from a file in another file, use
  	```html 
  	<div data-include="file_to_be_included.html"></div>
  	```
  	but please make sure that the script at `/assets/scripts/csi.min.js` is loaded. (This is generally included in headers of currently used files anyways, so there should be no problem if you use them as template)

----

## old 

* For viewing in mobile, although you must actually write adaptable css first
	~~~~html
	<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
	~~~~

* For Thai Language :  
	~~~~html
	<meta charset="UTF-8">
	~~~~

* For consistent font :  
	~~~~html
	<link href="https://fonts.googleapis.com/css?family=Karla:400,700" rel="stylesheet">
	~~~~

* For $\LaTeX$:  
	~~~~html
	<script type="text/x-mathjax-config">
  		MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});
	</script>
	<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-MML-AM_CHTML' async></script>
	~~~~
