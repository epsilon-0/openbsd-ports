COMMENT =	list files, recursively
DISTNAME =	lr-1.6
CATEGORIES =	sysutils

HOMEPAGE =	https://git.vuxu.org/lr/about/

MAINTAINER =	Evan Silberman <evan@jklol.net>

# MIT
PERMIT_PACKAGE =	Yes

WANTLIB += c

SITES =		https://git.vuxu.org/lr/snapshot/

MAKE_FLAGS =	CC="${CC}" CFLAGS="${CFLAGS}"

FAKE_FLAGS =	MANDIR="${PREFIX}/man"

NO_TEST =	Yes

.include <bsd.port.mk>
