COMMENT =	pager for the Blackbox window manager

DISTNAME =	bbpager-0.4.7
REVISION =	9

CATEGORIES =	x11
SITES =		${SITE_SOURCEFORGE:=bbtools/}

HOMEPAGE =	https://bbtools.sourceforge.net/

# GPLv2+
PERMIT_PACKAGE =		Yes

BUILD_DEPENDS = x11/blackbox

LIB_DEPENDS =	converters/libiconv

WANTLIB =	ICE SM X11 Xau Xdmcp Xext Xft Xrender c expat fontconfig \
		freetype iconv m ${COMPILER_LIBCXX} z xcb

COMPILER =		base-clang ports-gcc base-gcc

CONFIGURE_STYLE = gnu

.ifdef DEBUG
CONFIGURE_ARGS+=	--enable-debug
.endif

.include <bsd.port.mk>
