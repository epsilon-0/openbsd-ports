COMMENT =		SI6 networks IPv6 toolkit

VERSION =		2.0
DISTNAME =		ipv6toolkit-v${VERSION}
PKGNAME =		ipv6toolkit-${VERSION}
REVISION =		1

CATEGORIES =		net

HOMEPAGE =		http://www.si6networks.com/tools/ipv6toolkit/

MAINTAINER =		Alexander Bluhm <bluhm@openbsd.org>

# GPL v3
PERMIT_PACKAGE =	Yes

WANTLIB =		c m pcap

SITES =			http://www.si6networks.com/tools/ipv6toolkit/

MAKE_FLAGS =		CC=${CC}
FAKE_FLAGS =		PREFIX=${PREFIX} \
			MANPREFIX=${PREFIX} \
			ETCPATH=${DESTDIR}/${PREFIX}/share/examples/ipv6toolkit

NO_TEST =		Yes

pre-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/ipv6toolkit

.include <bsd.port.mk>
