COMMENT=		reimplementation of Dan Bernstein's daemontools#'

DISTNAME=		freedt-23
CATEGORIES=		sysutils
REVISION=		2

HOMEPAGE=		http://offog.org/code/freedt.html

# ISC
PERMIT_PACKAGE=	Yes

WANTLIB=		c

SITES=			http://offog.org/files/

CONFIGURE_STYLE=	gnu

post-install:
	rm -f ${PREFIX}/bin/recordio
	mv ${PREFIX}/bin/{,f}argv0

.include <bsd.port.mk>
