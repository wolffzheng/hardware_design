# install and dist
dist_doc_DATA = manual.pdf

# dist
EXTRA_DIST  = manual.lyx Tables Images

MAINTAINERCLEANFILES = manual.pdf

lyx_fragments := \
	 $(wildcard Tables/*.lyx) \
	 $(wildcard Images/*.png) \
	 $(wildcard Images/*.gif)

manual.pdf : manual.lyx $(lyx_fragments)
	rm -f $@ ; lyx --export pdf2 $<

upload:
	chmod 664 manual.pdf
	scp manual.pdf web.sourceforge.net:htdocs/docs
	echo "ls -l htdocs/docs" | sftp web.sourceforge.net
