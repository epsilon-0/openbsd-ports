# $OpenBSD: Makefile,v 1.32 2019/07/12 20:47:42 sthen Exp $

COMMENT=	library of Fortran linear algebra subroutines

CATEGORIES=	math devel

VERSION=	3.9.0
GH_ACCOUNT=	Reference-LAPACK
GH_PROJECT=	lapack
GH_TAGNAME=	v${VERSION}

SHARED_LIBS=	lapack 7.2 \
		lapacke 7.2 \
		blas 7.2 \
		cblas 7.2

HOMEPAGE=	http://www.netlib.org/lapack/

MAINTAINER=	Steven Mestdagh <steven@openbsd.org>

# BSD
PERMIT_PACKAGE=	Yes

WANTLIB+=	m

MODULES=	devel/cmake fortran
MODFORTRAN_COMPILER = gfortran
BUILD_DEPENDS=	${MODFORTRAN_BUILD_DEPENDS} \
		devel/doxygen

CONFIGURE_ARGS= 	-DCBLAS=ON \
			-DLAPACKE=ON \
			-DBUILD_SHARED_LIBS=ON \
			-DBUILD_TESTING=OFF

post-patch:
	cd "${WRKSRC}" && CLANG_ASSISTED_PARSING=Yes \
		doxygen -u DOCS/Doxyfile_man

post-build:
	cd "${WRKSRC}" && doxygen DOCS/Doxyfile_man

post-install:
	cd "${WRKSRC}" && \
		${INSTALL_MAN} DOCS/man/man3/* ${PREFIX}/man/man3

.include <bsd.port.mk>
