cfgdir = $(DESTDIR)/etc/eventwatchd
bindir = $(DESTDIR)/usr/bin

cpiop = find  . ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 | \
	cpio -0pd

install-exec-hook:
	mkdir -p $(cfgdir)
	cp doc/eventwatchd.conf.sample $(cfgdir)/eventwatchd.conf.sample
	mkdir -p $(bindir)
	cp src/eventwatchd.pl $(bindir)/eventwatchd
	chmod 755 $(bindir)/eventwatchd
