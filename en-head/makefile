STARDICT_TOOLS_DIR=~/stardict/tools/src/
TABFILE=$(STARDICT_TOOLS_DIR)/tabfile
DICT_TOOLS_BIN_BASH=~/dict-tools/bin/bash

# make all DICTS=xyz
DICTS=.*

.PHONY: all stardict tars

all:final_babylon stardict tars

final_babylon:
	bash $(DICT_TOOLS_BIN_BASH)/babylon_add_optitrans.sh DICTS=$(DICTS)

stardict:
	bash $(DICT_TOOLS_BIN_BASH)/tsv_to_stardict.sh DICTS=$(DICTS)


tars:
	bash $(DICT_TOOLS_BIN_BASH)/make_tarballs.sh https://github.com/indic-dict/stardict-hindi/raw/gh-pages/$(shell pwd|sed -e s/.*stardict-[^/]*[/]//)/tars DICTS=$(DICTS)
