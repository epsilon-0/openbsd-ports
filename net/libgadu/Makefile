COMMENT=	implementation of Gadu-Gadu IM protocol

VER=		1.12.2
DISTNAME=	libgadu-${VER}
EPOCH=		0
CATEGORIES=	net
SITES=		http://github.com/wojtekka/libgadu/releases/download/${VER}/

SHARED_LIBS=	gadu	7.0

HOMEPAGE=	http://libgadu.net/

# LGPLv2.1
PERMIT_PACKAGE=	Yes

WANTLIB=	pthread z

USE_GMAKE=	Yes
CONFIGURE_STYLE=gnu
CONFIGURE_ARGS=	--disable-tests \
		--without-bind \
		--without-gnutls \
		--without-openssl \
		--without-protobuf
CONFIGURE_ENV=	ac_cv_prog_DOXYGEN=no

NO_TEST=	Yes

.include <bsd.port.mk>
