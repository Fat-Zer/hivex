# hivex
# Copyright (C) 2010 Red Hat Inc.
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 675 Mass Ave, Cambridge, MA 02139, USA.

EXTRA_DIST = \
	hivexregedit

bin_SCRIPTS = hivexregedit

man_MANS = hivexregedit.1

hivexregedit.1: hivexregedit
	$(POD2MAN) \
	  --section 1 \
	  -c "Windows Registry" \
	  --name "hivexregedit" \
	  --release "$(PACKAGE_NAME)-$(PACKAGE_VERSION)" \
	  $< > $@-t; mv $@-t $@

noinst_DATA = \
	$(top_builddir)/html/hivexregedit.1.html

$(top_builddir)/html/hivexregedit.1.html: hivexregedit
	mkdir -p $(top_builddir)/html
	cd $(top_builddir) && pod2html \
	  --css 'pod.css' \
	  --htmldir html \
	  --outfile html/hivexregedit.1.html \
	  regedit/hivexregedit

CLEANFILES = $(man_MANS)
