# $OpenBSD: $

COMMENT =	C++17 wrapper for Lightning Memory-Mapped Database

VERSION =	1.0.0
PKGNAME =	lmdbxx-${VERSION}
DISTNAME =	${PKGNAME}

CATEGORIES =	databases

GH_ACCOUNT =	hoytech
GH_PROJECT =	lmdbxx
#GH_TAGNAME =	1.0.0
GH_COMMIT =	f1f00acf5f5045b43d7189c2b23ae5ca103a6faa

HOMEPAGE =	https://github.com/hoytech/lmdbxx

MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# Unlicense
PERMIT_PACKAGE =	Yes

COMPILER =	base-clang

NO_BUILD =	Yes

RUN_DEPENDS =	databases/lmdb

do-install:
	cd ${WRKSRC} && \
	mkdir -p ${PREFIX}/include && \
	${INSTALL_DATA} lmdb++.h ${PREFIX}/include 

do-test:
	cd ${WRKSRC} && \
	rm -rf testdb && \
	mkdir -p testdb && \
	${CXX} ${CXXFLAGS} -std=c++17 -Wall -I${LOCALBASE}/include -I. \
		-o check check.cc ${LDFLAGS} -L${LOCALBASE}/lib -llmdb && \
	./check

.include <bsd.port.mk>
