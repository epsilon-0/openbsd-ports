COMMENT=		Visual Tcl development environment

DISTNAME=		vtcl-1.6.1a1
REVISION=		2
CATEGORIES=		devel
MAINTAINER =		Stuart Cassoff <stwo@users.sourceforge.net>

HOMEPAGE=		https://vtcl.sourceforge.net/

# GPLv2+
PERMIT_PACKAGE=	Yes

SITES=			${SITE_SOURCEFORGE:=vtcl/}

MODULES=		x11/tk
NO_BUILD=		Yes
RUN_DEPENDS=		${MODTK_RUN_DEPENDS}

pre-patch:
	@cd ${WRKSRC}; perl -i -pe 's/\r$$//' `find . -type f`

do-install:
	rm ${WRKSRC}/lib/{propmgr,tkcon}.tcl${PATCHORIG}
	${INSTALL_DATA_DIR} ${PREFIX}/lib/vtcl
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/vtcl
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/vtcl
	cp -R ${WRKSRC}/vtcl.tcl ${WRKSRC}/images ${WRKSRC}/lib \
	     ${WRKSRC}/demo ${PREFIX}/lib/vtcl
	cp -R ${WRKSRC}/sample ${PREFIX}/share/examples/vtcl
	cp -R ${WRKSRC}/doc ${PREFIX}/share/doc/vtcl
	${SUBST_PROGRAM} ${FILESDIR}/vtcl ${PREFIX}/bin/vtcl

NO_TEST=		Yes

.include <bsd.port.mk>
