STARDICT_TOOLS_DIR=~/stardict/tools/src/
TABFILE=$(STARDICT_TOOLS_DIR)/tabfile
STARDICT_SANSKRIT_BIN=~/stardict-sanskrit/bin

ifndef dicts
	dicts="*"
endif

.PHONY: all tars decompile dunzip

all:add_optitrans stardict tars

stardict:
	bash $(STARDICT_SANSKRIT_BIN)/tsv_to_stardict.sh 

add_optitrans:
	bash $(STARDICT_SANSKRIT_BIN)/babylon_add_optitrans.sh 

tars:
	bash $(STARDICT_SANSKRIT_BIN)/make_tarballs.sh https://github.com/sanskrit-coders/stardict-hindi/raw/master/hi-head
	
decompile:
	bash ./decompile_all.sh
