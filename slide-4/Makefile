##################################################
#            INTRO TO MAKE: SLIDE 4              #
##################################################

# We can also store variables.
IN  = src
OUT = dist

all: $(OUT)/post.html

# The % symbol does pattern matching
$(OUT)/%.html: $(IN)/%.md
	markdown $^ > $@
