COMMENT=	look at the icmp messages received by the host

DISTNAME=	icmpinfo-1.11
REVISION=	0
CATEGORIES=	net sysutils

SITES=		${SITE_SUNSITE:=system/network/admin/}

PERMIT_PACKAGE=	Yes
WANTLIB=		c

ALL_TARGET=

NO_TEST=	Yes

do-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/icmpinfo
	${INSTALL_PROGRAM} ${WRKSRC}/icmpinfo ${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/icmpinfo.man ${PREFIX}/man/man1/icmpinfo.1
	${INSTALL_DATA} ${WRKSRC}/README ${PREFIX}/share/doc/icmpinfo

.include <bsd.port.mk>
