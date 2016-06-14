##################################################
#            INTRO TO MAKE: SLIDE 6              #
##################################################

IN  = src
OUT = dist

# Make comes with a variety of helper functions
DOCS  = $(wildcard $(IN)/*.md)
PAGES = $(patsubst $(IN)/%.md,$(OUT)/%.html,$(DOCS))

all: $(PAGES)

# The % symbol does pattern matching
$(OUT)/%.html: $(IN)/%.md
	markdown $^ > $@

clean:
	rm -rf $(OUT)/*

.PHONY: clean
