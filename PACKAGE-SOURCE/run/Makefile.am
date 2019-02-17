runstate_DATA = default.locale
CLEANFILES = $(runstate_DATA)
EXTRA_DIST = default.locale.in


do_subst = sed -e  's,[@]datadir[@],$(datadir),g' \
	-e 's,[@]runstatedir[@],$(runstatedir),g' \
	-e 's,[@]PACKAGE[@],$(PACKAGE),g' \
	-e 's,[@]VERSION[@],$(VERSION),g'

default.locale : default.locale.in Makefile
	$(do_subst) < $(srcdir)/$< > $@
	chmod -x $@
	chmod o-w $@
	chmod g+w $@

