# $OpenBSD: Makefile,v 1.7 2021/03/07 02:25:06 daniel Exp $

COMMENT =	convert between traditional and simplified Chinese

V =		1.1.1
DISTNAME =	opencc-$V
REVISION =	0

GH_ACCOUNT =	BYVoid
GH_PROJECT =	OpenCC
GH_TAGNAME =	ver.$V

SHARED_LIBS +=  opencc                    0.0 # 1.0

CATEGORIES =	converters textproc

HOMEPAGE =	https://opencc.byvoid.com/

MAINTAINER =	Anthony J. Bentley <anthony@anjbe.name>

# Apache 2.0
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} c m

COMPILER =		base-clang ports-gcc
MODULES =		devel/cmake \
			lang/python

MODPY_RUNDEP =		No

WRKDIST =		${WRKDIR}/OpenCC-ver.$V

.include <bsd.port.mk>
