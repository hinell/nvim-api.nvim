export NVIM=nvim
export SHELL=/usr/bin/bash
export MODULE_NAME ?=nvim-api
###############################################################################

# This file intended to be run from root of the project
# doc/Makefile.vimdoc.in
# doc: setup ts-vimdoc.nvim targets to generate vimhelp from markdown
#-------------------------------------

$(info $(shell pwd))
# static rules to convert .md to .txt files for vimdoc
include ../tools/make/ts-vimdoc.mk

# Add more files here,
# e.g. $(MODULE_NAME)-subpage.txt - will be made out of $(MODULE_NAME)-subpage.md
.ONESHEL:
tags: $(MODULE_NAME).txt
	@$(NVIM) --headless -c "helptags ./" -c "q!"

.PHONY: clean
.ONESHELL:
clean:
	rm -v $(MODULE_NAME).txt ./tags

all: tags
