COMMENT =	free multi-dimensional Tetris-like game
DISTNAME =	galois-0.6
REVISION =	1
CATEGORIES =	games x11

HOMEPAGE =	https://www.nongnu.org/galois/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# GPLv3+
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} atk-1.0 atkmm-1.6 c cairo cairo-gobject
WANTLIB += cairomm-1.0 fribidi gdk-3 gdk_pixbuf-2.0 gdkmm-3.0
WANTLIB += gio-2.0 giomm-2.4 glib-2.0 glibmm-2.4 gobject-2.0 gtk-3
WANTLIB += gtkmm-3.0 intl m pango-1.0 pangocairo-1.0 pangomm-1.4
WANTLIB += sigc-2.0 xml++-2.6 xml2 harfbuzz

SITES =		${SITE_SAVANNAH:=galois/source/}

# C++14
COMPILER =	base-clang ports-gcc

LIB_DEPENDS =	textproc/libxml++>=2.40.0 \
		x11/gtk3mm

RUN_DEPENDS =	devel/desktop-file-utils

CONFIGURE_STYLE =	gnu

MAKE_FILE =	makefile
ALL_TARGET =	default
MAKE_FLAGS =	CXX="${CXX}" CXXFLAGS="${CXXFLAGS} -std=c++14"

NO_TEST =	Yes

.include <bsd.port.mk>
