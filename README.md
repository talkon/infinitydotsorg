# infinitydotsorg

This repository hosts the files for https://infinitydots.org.
## About the website

* The website is currently hosted on GitHub Pages, which is FREE and only allows hosting of static websites, and has a soft limit of 1GB storage and 100GB bandwidth. We are nowhere near these limits, nor are we planning to do anything dynamic with our website, so everything should be fine.
* The published branch is `gh-pages`, not `master`, and the website is built from `docs/`. Generally, work on `master` until you are sure the changes can go online, then merge `master` into `gh-pages` to update the site.
* talkon owns the domain https://infinitydots.org and plans to renew it indefinitely.
* The site was redesigned in January 2020. Files for the old site (which has more content, actually) can be find in the `old-2019/` directory.

## Contributing

Contributions to this repository are very welcome. 

For a guideline of what we are (or were) planning to do, see the subsections below.
Things we planned to do reasonably soon are marked with **TODO**; things we planned to eventually include are marked **PLAN**; things we dreamt of doing are marked **DREAM**.

Of course, contributions not included in the to-do list below are also welcomed!
### Content

The minimal upkeep we need is to keep the Archive page updated at least once a year or so. Unless we have significantly more contributor-hours devoted to the site, that's probably all we can realistically do.
* > **[TODO]**: Add Oct Camp 2020 and TST 2021 to archive; the tests can be found [here.](https://www.dropbox.com/sh/edw8cdk3nnvasyr/AAAA6S06NXZaTIbqTwmuofN1a/2020-2021/ข้อสอบ?dl=0&subfolder_nav_tracking=1)
* **[PLAN]**: Keep a database of problems in $\TeX$ with metadata such as contest, year, subject, difficulty, topics used; auto-generate tests/exams/problem sets based on these attributes.
* **[PLAN]**: Create Thai and English versions for all our files.
* **[DREAM]**: Write up (unofficial) solutions to exams.
* **[DREAM]**: Port and revive blog if there is enough interest.
* **[DREAM]**: Run a weekly/monthly problems page similar to https://www.aldaily.com but with the columns for easy/medium/hard problems.

### Design

Design principle: each page shold have a background color (ex. black), a text color (white), and a tint color (red). Special texts should be somewhere between the text and the tint color.
`red.css` is the currently used CSS file. `red_old.css`, as its name says, defines the old style before the redesign.
See current pages (ex. mo.html) for example of divs to be used.
* > **[TODO]**: Adjust screen width cutoff; site should be in no-sidebar mode for slightly larger widths
* **[PLAN]**: Convert the above to LESS, and upgrade the site from CSS to LESS. This allows us to easily change the tint-color, for example, blue for InfinityDots JMO pages if we'll ever have them again.
* **[DREAM]**: Animate the logo on hover using SVG and CSS magic. Ideally the red (or whatever the tint color is) dots should rotate under the white infinity sign.
  * This is obviously more for artistic purposes than for any useful purpose, but it'd look nice.
## Tips
### Getting started

* **Setting up a local repository.** Due to how Git works, you need to clone this (online) repository to your computer to edit. The easiest way is to use [GitHub Desktop](https://desktop.github.com). If you do not have edit access to this repository, you can fork it and submit a pull request later.
* **Git basics.** These are things you need to do when editing the site:
  * Before starting, **fetch origin** to make sure your local repo is up-to-date.
  * After you finish, **commit** to ensure your edits are recorded, then **push to origin** to push your edits to the online repo.
* **The coding itself.** The site is coded in plain HTML with plain CSS<sup>(might be updated to LESS soon)</sup> for style. Resources for these languages can easily be found online. Google is your best friend.

### Other tips
* To include code from a file in another file, use
  	```html 
  	<div data-include="file_to_be_included.html"></div>
  	```
  	but please make sure that the script at `/assets/scripts/csi.min.js` is loaded. (This is generally included in headers of currently used files anyways, so there should be no problem if you use them as template)
