COMMENT=	tty recorder

DISTNAME=	ttyrec-1.0.8
REVISION=	4
CATEGORIES=	misc

HOMEPAGE=	http://0xcc.net/ttyrec/

# BSD
PERMIT_PACKAGE=	Yes

WANTLIB=	c

SITES=		http://0xcc.net/ttyrec/

NO_TEST=	Yes

BIN=	ttyplay ttyrec ttytime

do-install:
	@cd ${WRKSRC} && ${INSTALL_PROGRAM} ${BIN} ${PREFIX}/bin
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/ttyrec
	${INSTALL_DATA} ${WRKSRC}/README ${PREFIX}/share/doc/ttyrec
	${INSTALL_MAN_DIR} ${PREFIX}/man/man1
	${INSTALL_MAN} ${WRKSRC}/*.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
