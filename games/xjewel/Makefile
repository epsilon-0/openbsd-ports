COMMENT=	dropping jewels game for X11

DISTNAME=	xjewel-1.6
REVISION =	7
CATEGORIES=	games
FIX_EXTRACT_PERMISSIONS=Yes

SITES=		${SITE_XCONTRIB:S/contrib/R5contrib/}
EXTRACT_SUFX=	.tar.z

PERMIT_PACKAGE=	Yes

WANTLIB=		X11 Xau Xdmcp Xext c xcb

MAKE_FLAGS=		HSCORE_FILE=/var/games/xjewel.scores \
			BINDIR='${PREFIX}/bin' \
			MANDIR='${PREFIX}/man/man6' \
			MANSUFFIX=6 \
			FFILE=pcf.gz

CONFIGURE_STYLE=imake
NO_TEST=	Yes

pre-install:
	${INSTALL_DATA_DIR} ${PREFIX}/lib/xjewel.font
	@cd ${WRKSRC}/bitmaps; ${INSTALL_DATA} seven_seg.pcf.gz \
		${PREFIX}/lib/xjewel.font

post-install:
	@mv ${PREFIX}/bin/xjewel ${PREFIX}/bin/xjewel_; \
	  echo "#!/bin/sh"				>  ${PREFIX}/bin/xjewel; \
	  echo "xset +fp ${TRUEPREFIX}/lib/xjewel.font"	>> ${PREFIX}/bin/xjewel; \
	  echo "xjewel_"				>> ${PREFIX}/bin/xjewel; \
	  chmod ugo+x ${PREFIX}/bin/xjewel
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/xjewel
	${INSTALL_DATA} /dev/null ${PREFIX}/share/examples/xjewel/xjewel.scores

.include <bsd.port.mk>
