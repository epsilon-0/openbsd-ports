# $OpenBSD: Makefile,v 1.6 2021/02/23 19:39:39 sthen Exp $

BROKEN-i386 =	uint128_t

COMMENT =	reverse engineering framework in Python

MODPY_EGG_VERSION = 0.1.3_pl20210304
DISTNAME =	miasm-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}

EPOCH =		0

GH_ACCOUNT =	cea-sec
GH_PROJECT =	miasm
GH_COMMIT =	43fef27b4e21b5ad5d592733d1989c22e2cfff28

CATEGORIES =	security devel

HOMEPAGE =	https://github.com/cea-sec/miasm

MAINTAINER =	Remi Pointel <rpointel@openbsd.org>

# GPLv2
PERMIT_PACKAGE =	Yes

MODULES =	lang/python
FLAVORS =	python3
FLAVOR =	python3

WANTLIB += 	pthread ${MODPY_WANTLIB}

RUN_DEPENDS =	devel/angr/py-z3-solver \
		devel/py-cparser${MODPY_FLAVOR} \
		devel/py-future${MODPY_FLAVOR} \
		devel/py-llvmlite${MODPY_FLAVOR} \
		devel/py-parsing${MODPY_FLAVOR}

post-build:
	${MODPY_BIN} ${MODPY_LIBDIR}/compileall.py ${WRKSRC}/example

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/${MODPY_PY_PREFIX}miasm
	cp -r ${WRKSRC}/example ${PREFIX}/share/${MODPY_PY_PREFIX}miasm/

# this takes **really** long
do-test:
	cd ${WRKSRC}/test && \
		PYTHONPATH="..:../.." \
		${MODPY_BIN} ./test_all.py

.include <bsd.port.mk>
