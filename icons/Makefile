APPNAME := ojuba-logo-icon

ECHO := echo
NAKE := make
PYTHON := python2
INSTALL := install
INTLTOOL_MERGE := intltool-merge
RM := $(shell which rm | egrep '/' | sed  's/\s//g')


all: icons
	@$(ECHO) "*** done!"

icons:
	@$(ECHO) "*** Creating icons..."
	@for i in 256 96 48 36 32 24 16; do \
		$(INSTALL) -d hicolor/$${i}x$${i}/apps; \
		convert -background none $(APPNAME).svg -resize $${i}x$${i} hicolor/$${i}x$${i}/apps/$(APPNAME).png; \
	done
	@convert -background none anaconda.svg -resize 48x48 hicolor/48x48/apps/anaconda.png; \
	
	@$(INSTALL) -d hicolor/scalable/apps;
	@$(INSTALL) -m 0644 -D *.svg hicolor/scalable/apps/; \
	

clean:
	@$(ECHO) "*** Cleaning..."
	@$(RM) -rf hicolor
	
