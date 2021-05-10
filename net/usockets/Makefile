# $OpenBSD: Makefile,v 1.5 2020/12/11 22:34:51 sthen Exp $

COMMENT	=	eventing, networking & crypto for async applications
CATEGORIES =	net

VERSION =	0.7.1

DISTNAME =	usockets-${VERSION}
PKGNAME =	${DISTNAME:L}

SHARED_LIBS =	usockets 1.1

GH_ACCOUNT =	uNetworking
GH_PROJECT =	uSockets
#GH_TAGNAME =	v0.7.1
# socket read/write error
GH_COMMIT =	5440dbac79bd76444175b76ee95dfcade12a6aac

MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# Apache 2.0
PERMIT_PACKAGE =	Yes

WANTLIB +=	${COMPILER_LIBCXX} crypto ssl uv

# C11 C++17
COMPILER =	base-clang ports-gcc

LIB_DEPENDS =	devel/libuv

MAKE_ENV =	LIBusockets_VERSION="${LIBusockets_VERSION}"

NO_TEST =	Yes

FAKE_FLAGS =	PREFIX=${TRUEPREFIX}

.include <bsd.port.mk>
