STARDICT_TOOLS_DIR=~/stardict/tools/src/
TABFILE=$(STARDICT_TOOLS_DIR)/tabfile
STARDICT_SANSKRIT_BIN=~/stardict-sanskrit/bin

# make all DICTS=xyz
DICTS=.*

.PHONY: all stardict tars

all:final_babylon stardict tars

final_babylon:
	bash $(STARDICT_SANSKRIT_BIN)/babylon_add_optitrans.sh DICTS=$(DICTS)

stardict:
	bash $(STARDICT_SANSKRIT_BIN)/tsv_to_stardict.sh DICTS=$(DICTS)

	
tars:
	bash $(STARDICT_SANSKRIT_BIN)/make_tarballs.sh https://github.com/sanskrit-coders/stardict-hindi/raw/master/$(shell pwd|sed -e s/.*[/]//) DICTS=$(DICTS)

