COMMENT=		network statistics gatherer with graphs

PORTROACH=		site:https://github.com/emikulic/darkstat/archive/

DISTNAME=		darkstat-3.0.719
CATEGORIES=		net www
SITES=			${HOMEPAGE}
EXTRACT_SUFX=		.tar.bz2
REVISION=		3

HOMEPAGE=		https://unix4lyfe.org/darkstat/

# GPLv2 and BSD
PERMIT_PACKAGE=	Yes

WANTLIB=		c pcap z

CONFIGURE_STYLE=	autoconf
AUTOCONF_VERSION=	2.69
CONFIGURE_ARGS=		--with-privdrop-user=_darkstat

NO_TEST=		Yes

.include <bsd.port.mk>
