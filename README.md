
## WIP Documentation
v 0.1

This documentation is a work in progress. It is being researched, planned, and tested.

License: https://creativecommons.org/licenses/by/4.0/
Feel free to fork or make suggestions.

--

# Branch Structure

* `master` - This is our base branch for development.
* `feature-XXX` - Individual branches for development. Branches from 'master' branch.
* `bug-XXX` - Branches for hotfixes, developmental bug fixes, etc. Branches from 'master' or 'stable' branch. These are generally for fixing things on live sites.
* `stable` - This branch gets incremented whenever the production environment gets updated. This allows us to work backwards through iterations to find bug sources.


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

* Individual bug fixes and features need to be committed when they are completed. This keeps our commits better organized and aids in collaboration and merges.
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
