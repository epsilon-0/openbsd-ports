COMMENT=	format/convert text documents into compressed .pdb files

VERSION=	0.9.4
PROG=		bibelot
DISTNAME=	${PROG}-${VERSION}
CATEGORIES=	textproc
REVISION=	3

PERMIT_PACKAGE=	Yes

HOMEPAGE=	https://sourceforge.net/projects/bibelot

SITES=		${SITE_SOURCEFORGE:=bibelot/}

NO_BUILD=	Yes
NO_TEST=	Yes
PKG_ARCH=	*
WRKDIST=	${WRKDIR}/${PROG}

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/${PROG}.pl ${PREFIX}/bin/${PROG}
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/${PROG}
	${INSTALL_DATA} ${WRKSRC}/README ${PREFIX}/share/doc/${PROG}

.include <bsd.port.mk>
