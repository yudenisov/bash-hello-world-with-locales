bin_SCRIPTS = hello-world.sh set-default-helloworld-locales.sh
CLEANFILES = $(bin_SCRIPTS)
EXTRA_DIST = hello-world.in set-default-helloworld-locales.in


do_subst = sed -e  's,[@]datadir[@],$(datadir),g' \
	-e 's,[@]runstatedir[@],$(runstatedir),g' \
	-e 's,[@]PACKAGE[@],$(PACKAGE),g' \
	-e 's,[@]VERSION[@],$(VERSION),g'

hello-world.sh : hello-world.in Makefile
	$(do_subst) < $(srcdir)/$< > $@
	chmod +x $@
	chmod o-w $@
	chmod g-w $@

set-default-helloworld-locales.sh : set-default-helloworld-locales.in Makefile
	$(do_subst) < $(srcdir)/$< > $@
	chmod +x $@
	chmod o-w $@
	chmod g-w $@

