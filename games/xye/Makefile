COMMENT =	puzzle game collecting diamonds and avoiding obstacles
DISTNAME =	xye-0.12.2
CATEGORIES =	games x11
REVISION =	5

HOMEPAGE =	https://xye.sourceforge.net/
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# zlib
PERMIT_PACKAGE =	Yes

SITES =		${SITE_SOURCEFORGE:=xye/}

FIX_CRLF_FILES =	src/xsb_level.cpp

WANTLIB += SDL SDL_image SDL_ttf c m pthread ${COMPILER_LIBCXX}

COMPILER =		base-clang ports-gcc base-gcc

LIB_DEPENDS =	devel/sdl-image \
		devel/sdl-ttf

RUN_DEPENDS =	devel/desktop-file-utils

CONFIGURE_STYLE =	gnu

.include <bsd.port.mk>
