##################################################
#            INTRO TO MAKE: SLIDE 7              #
##################################################

IN    = src
OUT   = dist
DOCS  = $(wildcard $(IN)/*.md)
PAGES = $(patsubst $(IN)/%.md,$(OUT)/%.html,$(DOCS))

# Tell make to build in parallel. += says append
MAKEFLAGS += "-j 4"

# ?= says only assign if it hasn't already been set
PORT ?= 4000

all: $(PAGES)

# By default, Make reports everything it does. This can
# be pretty noisy.
#
# "Silence is golden" - http://www.linfo.org/rule_of_silence.html
#
# @ at the beginning of a line prevents this output
$(OUT)/%.html: $(IN)/%.md
	@ markdown $^ > $@
	@ echo "[+] $*"

watch: all
	@ echo "[+] Watching $(IN)"
	@ fswatch -o $(IN) | xargs -n1 -I{} make

serve: all
	@ python -m SimpleHTTPServer $(PORT)

clean:
	@ rm -rf $(OUT)/*

.PHONY: clean serve watch
