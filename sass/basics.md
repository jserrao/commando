## Compass partials you want:

@import "compass/support";						// Add Compass' IE and vendor prefix support variables.
@import "compass/utilities/general/clearfix";	// Better than Drupal's clearfix
@import "compass/utilities/sprites";			// Helps with sprites (http://compass-style.org/help/tutorials/spriting)
@import "compass/css3";							// Use one CSS3 mixin instead of multiple
@import "compass/typography/vertical_rhythm"; 	// Helps set up vertical rhythm
@import "zen";									// Add zen grids responsive layout mixins.


## pseudo classes need ampersands if they are nested in SASS
a.newtab {
	text-decoration: none;
	color: blue;

	&:hover {
		text-decoration: underline;
		color: $callout-red;
	}
}

## put IE specific styles with the ampersand underneath 
#main {
	background: $light-gray;
	.lt-ie9 &{
		background: $dark-orange;
	}
}

## mixin is a CSS function more or less - you have a mixin folder with functions you will call later in the land of SASS
mixin {
	background: $orange;
	font: $helvetica;
}
