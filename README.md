
## WIP Documentation
v 0.2

This documentation is a work in progress. It is being researched, planned, and tested.

License: https://creativecommons.org/licenses/by/4.0/
Feel free to fork or make suggestions.

--

# Branch Structure

* `development` - This is our base branch for development/testing. Feature and bug 
* `feature-XXX` - Individual branches for development. Branches from 'development' branch.
* `bug-XXX` - Branches for hotfixes, developmental bug fixes, etc. Branches from 'master' or 'development' branch. These branches are generally for testing and fixing things on live sites.
* `master` - This branch gets incremented whenever the production environment gets updated. Use Release Tags for stable releases, this allows us to work backwards through iterations to find bug sources.

The master branch should use [tags](https://help.github.com/articles/working-with-tags/) to keep track of project updates. 

* `X.Y.Y` - X designates major upgrades to the site. Redesigns, refreshes, major site rollouts. 
* `Y.X.Y` - X designates site updates that add new functionality but isn't considered "major" new functionality.
* `Y.Y.X` - X designates bug fixes, content changes, and optimization tweaks.


# Use Feature Branches

* All work should be performed in branches (feature or bug) outside of Master.
* Branches should be feature focused when collaborating.
	* Keep feature branches focused. Don't jump all over the place. In particular, do not perform work on another feature that has an existing branch.
* Branches should be named after the feature that is being worked on, designated as feature or bug.
	* Example: `feature-gallery`
	* Example: `bug-horizontal-scrollbar-gallery`
* Feature branches need to stay segmented. Don't work on different features within a singular branch.
* Changes must be tested before pulled into the master branch.


# Commits should be frequent

* Individual tasks, features, and bug fixes need to be committed when they are completed. This keeps our commits better organized and aids in collaboration and merges.
	* Example: If you complete your work on a blog post page, commit that work before moving onto the contact page.
* Never leave for the day with un-committed changes.
* Perform a pull from the 'master' branch with every commit.
* Perform a pull from master when starting work on the project to ensure you're up to date.
* Commit logs need to be detailed.
	* The commit Summary should be understandable by a third party as best as possible.
	* The commit Description should explain what you did and why. If it is for an assigned task, reference the task URL. If there is no task, consider creating a task to reference
	* [Chris Beams - How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)


# All code must be written as components to avoid conflicts

* Make sure code stays isolated to prevent messing with other sections of the website.
* Components should be named after their structure and/or functionality, not the content in them.
	* Example: `full-width-cta` not `learn-about-our-services`
* Use lots of code notes. The more you explain your code for your future self and coworkers, the better.
	* Comments should not be done in a way it ends up on the end site.
	* Example: In SASS and JS, use `//` so it gets compiled out.
	* Example: In HTML/PHP, use PHP comments so it gets compiled out.


# Working with WordPress

When working on WordPress themes and plugins, use the [Github Updater plugin](https://github.com/afragen/github-updater/). Incrementing the theme version number in style.css allows for easy site updates with no downtime. 
