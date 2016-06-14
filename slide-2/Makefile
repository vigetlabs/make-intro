##################################################
#            INTRO TO MAKE: SLIDE 2              #
##################################################

# Repeating yourself feels bad. This is build automation!

# Make has the concept of automatic variables:
dist/post.html: src/post.md
	markdown $^ > $@

# $@ is the name of the build target (dist/colors)
# $^ is short for all of the the dependencies (src/red src/blue)
