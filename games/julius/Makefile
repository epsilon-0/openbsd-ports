V =		1.7.0
COMMENT =	open source re-implementation of Caesar III game engine
DISTNAME =	julius-${V}
EXTRACT_SUFX =	-source.tar.gz
CATEGORIES =	games x11
REVISION =	0

HOMEPAGE =	https://github.com/bvschaik/julius
MAINTAINER =	Brian Callahan <bcallah@openbsd.org>

# AGPLv3 only
PERMIT_PACKAGE =	Yes

WANTLIB += SDL2 SDL2_mixer c m png pthread z

SITES =		https://github.com/bvschaik/julius/releases/download/v${V}/

MODULES =	devel/cmake

LIB_DEPENDS =	devel/sdl2-mixer \
		graphics/png

RUN_DEPENDS =	devel/desktop-file-utils \
		x11/gtk+4,-guic

# Talk to upstream about this?
pre-configure:
	sed -i 's,--coverage,,g' ${WRKSRC}/test/CMakeLists.txt

.include <bsd.port.mk>
