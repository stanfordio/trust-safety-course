all: 
	$(foreach file, $(wildcard *.tex), latexmk -pdflatex=lualatex -pdf $(file);)
	mv *.pdf pdf/

crunch:
	mkdir -p img-orig
	cp -av img/. img-orig/.
	pngquant -f --ext .png `find img -name "*.png"`

uncrunch:
	cp -av img-orig/. img/.
	rm -rf img-orig

clean:
	-rm -f *.pdf pdf/*.pdf *.tmp *.out *.aux *.idx *.log *.ilg *.xref *.lg \
         *.toc *.ind *.4og *.4ct *.4tc *.idv *.lot *.lov *.lltr *.lstr \
         *.dvi *.odt *.rtf *.html *.snm *.nav *.fls tex4ht.env \
		 *.fdb_latexmk *.upa *.synctex* > /dev/null 2>&1
