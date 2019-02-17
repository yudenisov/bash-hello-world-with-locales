pkgdatadir = $(datadir)/@PACKAGE@
pkgdata_DATA = en-locale.txt ru-locale.txt
CLEANFILES = $(pkgdata_DATA)
EXTRA_DIST = en-locale.in ru-locale.in


do_subst = sed -e  's,[@]datadir[@],$(datadir),g' \
	-e 's,[@]runstatedir[@],$(runstatedir),g' \
	-e 's,[@]PACKAGE[@],$(PACKAGE),g' \
	-e 's,[@]VERSION[@],$(VERSION),g'

en-locale.txt : en-locale.in Makefile
	$(do_subst) < $(srcdir)/$< > $@
	chmod -x $@
	chmod o-w $@
	chmod g+w $@

ru-locale.txt : ru-locale.in Makefile
	$(do_subst) < $(srcdir)/$< > $@
	chmod -x $@
	chmod o-w $@
	chmod g+w $@

