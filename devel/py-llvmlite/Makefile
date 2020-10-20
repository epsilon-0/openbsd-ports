# $OpenBSD: Makefile,v 1.9 2020/08/22 22:06:01 naddy Exp $

COMMENT =	lightweight LLVM-Python binding for writing JIT compilers

MODPY_EGG_VERSION =	0.36.0
GH_ACCOUNT =	numba
GH_PROJECT =	llvmlite
GH_TAGNAME =	v${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}

CATEGORIES =	devel

MAINTAINER =	Remi Pointel <rpointel@openbsd.org>

HOMEPAGE =	http://llvmlite.pydata.org/

# BSD
PERMIT_PACKAGE =	Yes

WANTLIB +=	${COMPILER_LIBCXX} LLVM m

COMPILER =	base-clang
MODULES =	lang/python

FLAVORS =	python3
FLAVOR ?=	python3

MAKE_ENV +=	LLVM_CONFIG="/usr/bin/llvm-config" \
		LDLIBS="`llvm-config --libs all`" \
		CXXFLAGS="`llvm-config --cxxflags` -fPIC ${CFLAGS}" \
		LDFLAGS="`llvm-config --ldflags` ${LDFLAGS}"

pre-build:
	cd ${WRKSRC} && env -i ${MAKE_ENV} ${MAKE_PROGRAM} ${MAKE_FLAGS} \
		-f LIB_MAKEFILE

do-test:
	cd ${WRKSRC} && PYTHONPATH=. ${SETENV} ${MODPY_BIN} ./runtests.py

.include <bsd.port.mk>
