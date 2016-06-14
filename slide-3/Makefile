##################################################
#            INTRO TO MAKE: SLIDE 3              #
##################################################

# Let's make a default task. Make will always run
# the first task if not given any instructions
all: dist/post.html

# The % symbol does pattern matching
dist/%.html: src/%.md
	markdown $^ > $@
