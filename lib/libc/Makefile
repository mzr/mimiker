# vim: tabstop=8 shiftwidth=8 noexpandtab:

TOPDIR = $(realpath ../..)

CPPFLAGS = -I$(CURDIR) \
	   -I$(CURDIR)/include \
	   -I$(CURDIR)/citrus \
	   -I$(CURDIR)/gdtoa \
	   -I$(CURDIR)/gen \
	   -I$(CURDIR)/locale \
	   -I$(CURDIR)/stdlib \
	   -D_LIBC -DNO_FENV_H

SUBLIBS = citrus gdtoa gen locale misc regex stdio stdlib string sys termios time

SOURCES = $(foreach dir, $(SUBLIBS), \
            $(wildcard $(dir)/*.[cS]) $(wildcard $(dir)/$(ARCH)/*.S))

include $(TOPDIR)/build/build.lib.mk

$(SOURCES): assym.h

CLEAN-FILES += assym.h
