COMMENT =	weather in terminal, with ANSI colors and Unicode symbols

V =		1.19.0
DISTNAME =	ansiweather-$V

CATEGORIES =	astro

HOMEPAGE =	https://github.com/fcambus/ansiweather

# BSD
PERMIT_PACKAGE =	Yes

SITES =		https://github.com/fcambus/ansiweather/releases/download/$V/

RUN_DEPENDS =	textproc/jq

NO_BUILD =	Yes
NO_TEST =	Yes

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/ansiweather ${PREFIX}/bin
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/ansiweather
	${INSTALL_DATA} ${WRKSRC}/README.md ${PREFIX}/share/doc/ansiweather
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/ansiweather
	${INSTALL_DATA} ${WRKSRC}/ansiweatherrc.example \
		${PREFIX}/share/examples/ansiweather
	${INSTALL_DATA} ${WRKSRC}/ansiweather.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
