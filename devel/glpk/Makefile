COMMENT=	GNU Linear Programming Kit

DISTNAME=	glpk-5.0
SHARED_LIBS=	glpk		8.0	# 43.1.3

CATEGORIES=	devel
HOMEPAGE=	https://www.gnu.org/software/glpk/index.html
SITES=		${SITE_GNU:=glpk/}

# GPLv3
PERMIT_PACKAGE=	Yes

COMPILER=	base-clang ports-gcc
COMPILER_LANGS=	c

WANTLIB=		c m gmp

LIB_DEPENDS=		devel/gmp

CONFIGURE_STYLE=	gnu
CONFIGURE_ARGS=		--with-gmp
CONFIGURE_ENV=		CPPFLAGS="-I${LOCALBASE}/include" \
			LDFLAGS="-L${LOCALBASE}/lib"

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/glpk
	${INSTALL_DATA} ${WRKSRC}/doc/*.txt ${PREFIX}/share/doc/glpk
	${INSTALL_DATA} ${WRKSRC}/doc/*.pdf ${PREFIX}/share/doc/glpk
	${INSTALL_DATA_DIR} ${PREFIX}/share/doc/glpk/notes
	${INSTALL_DATA} ${WRKSRC}/doc/notes/*.pdf ${PREFIX}/share/doc/glpk/notes

.include <bsd.port.mk>
