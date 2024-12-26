MAKEFLAGS = --always-make
VALEOPTS = --no-wrap$(if $(LEVEL), --minAlertLevel=$(LEVEL))

check: $(shell find -name "*.md")

%.md:
	@echo
	vale $(VALEOPTS) $@ | sed -e '/^[[:space:]]*$$/d' -e 's|^|$@: &|'
