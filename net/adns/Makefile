COMMENT=		asynchronous dns resolver client library and utilities
DISTNAME=		adns-1.5.2

CATEGORIES=		net devel

SHARED_LIBS=		adns	2.0

HOMEPAGE=		https://www.chiark.greenend.org.uk/~ian/adns/

# GPLv3+
PERMIT_PACKAGE=	Yes

WANTLIB=		c

SITES=			https://www.chiark.greenend.org.uk/~ian/adns/ftp/

CONFIGURE_STYLE=	gnu dest
USE_GMAKE=		Yes
MAKE_FLAGS=		MAJOR=${LIBadns_VERSION:R} MINOR=${LIBadns_VERSION:E}

.include <bsd.port.mk>
