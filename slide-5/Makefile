##################################################
#            INTRO TO MAKE: SLIDE 5              #
##################################################

# .PHONY provides a way to say that tasks have no
# output and should aways run.

IN  = src
OUT = dist

all: $(OUT)/post.html

# The % symbol does pattern matching
$(OUT)/%.html: $(IN)/%.md
	markdown $^ > $@

clean:
	rm -rf $(OUT)/*

.PHONY: clean all
