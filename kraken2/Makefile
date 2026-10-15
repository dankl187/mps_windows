.PHONY: all install clean

SCRIPTS = scripts/*.sh \
	scripts/*.pl \
	scripts/*.pm \
	scripts/k2 \
	scripts/kraken2-build \
	scripts/kraken2 \
	scripts/kraken2-inspect

all:
	$(MAKE) -C src all

clean:
	$(MAKE) -C src clean

#install:
#	mkdir -p "$(KRAKEN2_DIR)" && \
#	cp $(SCRIPTS) "$(KRAKEN2_DIR)" && \
#	cd src && $(MAKE) install KRAKEN2_DIR="$(KRAKEN2_DIR)"
	
install:
	mkdir -p "$(KRAKEN2_DIR)" && \
	cp $(SCRIPTS) "$(KRAKEN2_DIR)" && \
	cd src && $(MAKE) all && cp classify.exe estimate_capacity.exe build_db.exe dump_table.exe lookup_accession_numbers.exe k2mask.exe blast_to_fasta.exe merge.exe "$(KRAKEN2_DIR)"

