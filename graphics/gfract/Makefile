BROKEN=			linking fails with Boost 1.76

COMMENT=		fractal program with GTK interface
GH_ACCOUNT=		oskusalerma
GH_PROJECT=		gfract
GH_TAGNAME=		v1.0
DISTFILES=		${DISTNAME}.tar.gz
DISTFILES.gfx=		gfract-palettes-0.1.tar.gz
CATEGORIES=		graphics math
REVISION=		4

HOMEPAGE=		http://www.oskusoft.com/programs/gfract/

# GPLv2+
PERMIT_PACKAGE=	Yes

WANTLIB += ${COMPILER_LIBCXX} X11 Xcomposite Xcursor Xdamage Xext
WANTLIB += Xfixes Xi Xinerama Xrandr Xrender atk-1.0 boost_filesystem
WANTLIB += boost_regex boost_system c cairo fontconfig freetype
WANTLIB += gdk-x11-2.0 gdk_pixbuf-2.0 gio-2.0 glib-2.0 gobject-2.0
WANTLIB += gtk-x11-2.0 harfbuzz intl m pango-1.0 pangocairo-1.0
WANTLIB += pangoft2-1.0 png z

COMPILER =		base-clang ports-gcc base-gcc

SITES.gfx= 		http://distfiles.sigtrap.nl/

MODULES=		lang/python

MODPY_RUNDEP=		No
MODPY_ADJ_FILES=	make_palettes.py
# override python module CONFIGURE_STYLE
CONFIGURE_STYLE=	none # empty

LIB_DEPENDS=		devel/boost \
			x11/gtk+2

USE_GMAKE=		Yes

NO_TEST=		Yes

ALL_TARGET=		gfract

MAKE_FLAGS=		CXX="${CXX}" CXXFLAGS="${CXXFLAGS}"

post-extract:
	cd ${WRKDIR} && mv monk2\'.map monk2.map

pre-build:
	sed -i.beforesubst 's,/usr/local,${LOCALBASE},' ${WRKSRC}/main.cpp

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/gfract/palettes
	${INSTALL_DATA} ${WRKDIR}/*.map ${PREFIX}/share/gfract/palettes/
	${INSTALL_DATA} ${WRKSRC}/gfract.xpm ${PREFIX}/share/gfract/
	${INSTALL_PROGRAM} ${WRKSRC}/gfract ${PREFIX}/bin/

.include <bsd.port.mk>
