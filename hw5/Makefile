T=hw5
BUILD=build.nosync

all: $(T).tex
	latexmk -xelatex -outdir=$(BUILD) $(T).tex
	cp $(BUILD)/$(T).pdf .
watch:
	latexmk -pvc -xelatex -outdir=$(BUILD) $(T).tex
plain:
	pandoc --to=plain --wrap=none $(T).tex > $(T).txt
purge:
	rm -rf $(BUILD)
clean: purge
	rm -f $(T).pdf
